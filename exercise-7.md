## Create a Flow that is triggered by a new Forms entry
In this exercise we will create our first Power Automate flow. The goal is to trigger the flow automatically when a new forms entry is created.

## Always start from the solution and create the flow
Go to the [Power Automate](https://make.powerautomate.com/) (or Power Apps) homepage, select the correct environment and select the solution you created earlier.
![power automate](/assets/7_powerautomate.png)

Create a new automated workflow.
![automated](/assets/7_automated.png)

## Select the trigger and create the flow
Give a meaningful name to the flow and select `When a new response is submitted` as the trigger. Click `Create`!
![create flow](/assets/7_createflow.png)

## Select the right form and get the response details
Select the Form we created earlier in the trigger.
![select form](/assets/7_selectform.png)

Select `+ New step`, type `response` into the search bar and select the Forms action `Get response details`
![get response](/assets/7_getresponse.png)

Selet the right Form again in this action and use the parameter `Response Id` from the previous step (coul look a litle different in your UI - the grey box is new...)
![attributes](/assets/7_selectattributes.png)

PLEASE SAVE YOUR FLOW!

## Initialize WorkshopID as a variable and set it depending on the selected workshop
We need to provide the Workshop ID to fill the `Workshop Title` LookUp field. To provide the ID we can set up a `Switch` action 

Select `+ New step` and initialize a variable.
![init variable](/assets/7_initvariable.png)

Call the variable `WorkshopID` and set the type to `Integer`
![name variable](/assets/7_namevariable.png)

Create a `Switch` Action
![switch](/assets/7_switch.png)

Add the response from the Forms question `Which Workshop would you like to attend?` as dynamic content
![which workshop](/assets/7_whichworkshop.png)

Chck in the `Workshops` list the IDs of your workshop (you probably need to unhide the ID column - it should start from 1)
![workshopids](/assets/7_workshopid.png)

Add as many cases as you have workshops and add the exact Workshop titles from SharePoint/Forms to the `Equals` field. Add a `Set variable` action for each Case, select the `WorkshopID` variable and fill in the corresponding IDs from SharePoint.
![switch setup](/assets/7_switchsetup.png)

## Switch

## Add Create item action
Select `+ New step`, type `create` into the search bar and select the `Create item`action from SharePoint.
![create](/assets/7_createitem.png)

Select the correct SharePoint-site as well as the `Registrations` list. The fields `Attendee` and `Workshop Title` should now appear on your screen.
![create parameters](/assets/7_createitemparameters.png)

![dynamic attendee](/assets/7_dynamicattendee.png)

![dynamic workshop](/assets/7_dynamicworkshop.png)

Your finished flow should look like this. Open your forms and send a test response.
![finished flow](/assets/7_finishedflow.png)

If the test went through, check your `Registrations` list. You should see a new entry with your user as `Attendee`.
![success](/assets/7_success.png)