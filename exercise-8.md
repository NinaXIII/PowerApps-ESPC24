# Create a Flow that sends a message to all attendees

In this exercise we want to create a flow that lets the organizer send a message to all participants of the workshop. The flow can be triggered directly from the SharePoint list.

## Did we already mention, that you should start from the solution to create your flows?

Of course we start from our solution. This time we create an instant flow. It will instantly run after triggering it manually.

![create automated](/assets/8_createautomated.png)

## Choose SharePoint Trigger and add input property

Choose a name like **Send a message to participants** and scroll down until you find the SharePoint trigger **for a selected item**.
![trigger item](/assets/8_chooseitemtrigger.png)

When you reach the editor select your SharePoint (over and over again) and select the list **Workshops**.

![list](/assets/8_chooselist.png)

Also we need to **Add an input** so we can input the message we want to send. Select **Text** as the type and name it `Message`.

![trigger](/assets/8_addtriggerinput.png)

## Get attendees

We will now get a list of the attendees of the selected workshop. Select the **Get items** action from SharePoint.

![quick start](/assets/8_getitems.png)

Select the correct SharePoint and use the list **Registrations**.
As a filter query we will use `WorkshopTitle/Id eq ` and then dynamically select the **ID** from the trigger. This will only return the Registrations for the Workshop with the same ID as the selected Workshop.

![quick start](/assets/8_getitemsfilter.png)

## Send an Email

Now you can use the Outlook action **Send an Email (v2)** to inform the attendees. As soon as you fill the field **To** with `Attendee Email` it will automatically (automagically) create an **Apply to each** loop around the action. Draft a quick message to the attendees and don't forget to include the **Message** attribute from the trigger.

![quick start](/assets/8_outlookoption.png)

## Variation: Send a Teams message

Another option would be to use the **Post message in a chat or channel** action from Microsoft Teams. This is the complete flow with the Teams action.

![completeflow](/assets/8_completeflowteams.png)

## Create a nice button in SharePoint

We could (and should) have used a Power Apps trigger for this Flow, but since this is the [ESPC](https://sharepointeurope.com), we will show you how to nicely integrate the trigger into your SharePoint list with the magic of list formatting.

Create a new dummy Text column in the **Workshops** list called `Start Flow` and select **Format Column** for it.

![quick start](/assets/8_formatcolumn.png)

Paste this JSON code into the text box and replace the Flow Identifier at the end:

```
{
  "$schema": "https://developer.microsoft.com/en-us/json-schemas/sp/column-formatting.schema.json",
  "elmType": "span",
  "style": {
    "border": "none",
    "background-color": "#ff69b4",
    "color": "#0078d7",
    "cursor": "pointer",
    "width": "100px",
    "margin": "5px",
    "border-radius": "20px",
    "visibility": "visible"
  },
  "children": [
    {
      "elmType": "button",
      "txtContent": "Notify Participants",
      "style": {
        "border": "none",
        "background-color": "transparent",
        "color": "white",
        "cursor": "pointer"
      },
      "customRowAction": {
        "action": "executeFlow",
        "actionParams": "{\"id\": \"FlowIdentifierGoesHere"}"
      }
    }
  ]
}
```

![quick start](/assets/8_formatting.png)

Exit the Flow editor and select **Export** and **Get Flow Identifier**. Copy the ID and replace `FlowIdentifierGoesHere` in your JSON.

![quick start](/assets/8_getidentifier.png)

## Test the Flow

Go to your Workshops list and select the button. Write a short dummy message and see if you receive a Teams message or Email.

![quick start](/assets/8_testflow.png)

![quick start](/assets/8_testsuccess.png)

You are awesome!
