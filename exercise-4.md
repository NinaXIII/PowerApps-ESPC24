# REST


## Part B: Creating the Browse Screen for Workshops

1. **Create a Browse Screen**:
   - Go to **+ Insert** > **New screen** > **List screen**
   - Rename the screen to `Browse Screen` by selecting the screen name in the left panel.

2. **Set Up the Gallery**:
   - By default, a gallery will be created on the screen. Select the gallery.
   - In the properties pane on the right, set **Items** to the **Workshops** data source
   - **Display Workshop Details**:
     - Select **Title** in the gallery and set the **Text** property to `ThisItem.'Workshop Title'`
     - Add a text label for **Date** and set its **Text** property to `ThisItem.Date`
     - Add a text label for **Capacity** and set its **Text** property to `ThisItem.Capacity`

3. **Navigate to Details Screen**:
   - Select the gallery and go to the **OnSelect** property
   - Set it to `Navigate(DetailScreen)`. (We’ll create this screen next.)

---

## Part C: Creating the Details Screen for Workshop Information

1. **Add a Details Screen**:
   - Go to **+ Insert** > **New screen** > **Detail screen**
   - Rename it `Detail Screen`

2. **Display Workshop Information**:
   - Select the **DetailForm** that appears on the screen
   - In the properties pane, set **Data Source** to `Workshops`
   - Select the **Item** property and set it to `BrowseGallery.Selected`.
   - Adjust the fields to display **Workshop Title**, **Date**, **Capacity**, and **Description**
   - Select on each field and choose **Edit fields** to show or hide fields as needed

3. **Add Back Button**:
   - Go to **+ Insert** > **Icon** > **Back arrow**
   - Set **OnSelect** to `Back()`. This allows users to return to the browse screen

## Part D: Creating the Registration Screen

1. **Add a Registration Screen**:
   - Go to **+ Insert** > **New screen** > **Form screen**
   - Rename it `Registration Screen`

2. **Set Up the Registration Form**:
   - Select the **Form** that appears on the screen
   - Set **Data Source** to `Registrations`
   - Under **Edit fields**, add the **Attendee Name**, **Email**, and **Workshop Title** fields
   - For **Workshop Title**, ensure it shows as a dropdown connected to the **Workshops** list

3. **Submit Button**:
   - Go to **+ Insert** > **Button**
   - Set the **Text** property to `"Submit Registration"`
   - Set **OnSelect** to:
  
     ```powerapps
     SubmitForm(RegistrationForm);
     Navigate(BrowseScreen)
     ```

   - This code saves the form data to the **Registrations** list and navigates back to the browse screen.

4. **Test the App**:
   - Run the app by selecting on **Preview** (Play icon)
   - Test viewing workshops, navigating to details, and submitting a registration
   - Verify that registrations are saved to the ***Registrations** list
