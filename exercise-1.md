# Exercise 1: Creating SharePoint Lists with Lookup Column

**Objective:** Create two SharePoint lists, **Workshops** and **Registrations**, and connect them with a lookup column to establish a pseudo relational data structure.

## Part A: Creating the **Workshops** List

1. **Navigate to SharePoint Home**: Go to your SharePoint site and select **New** > **List**
![create a List](/assets/espc24-createlist.png)

2. **Select Blank List**: Choose the option to create a blank list
3. **Name the List**: Enter the name **Workshops** and add a brief description, if needed. Select **Create**

4. **Add Columns to Workshops List**:
   - **Title Column** (automatically created): Rename this column to **Workshop Title**
   - **Date**:
     - Select **Add Column** > **Date and Time**
     - Name it **Date**
     - Select **Save**
   - **Capacity**:
     - Select **Add Column** > **Number**
     - Name it **Capacity** and set **Number of decimal places** to `0`
     - Select **Save**
   - **Description**:
     - Select **Add Column** > **Multiple lines of text**
     - Name it **Description**
     - Select **Save**

5. **Verify the List**: Ensure all columns are created as intended by viewing the list settings. You should see **Workshop Title**, **Date**, **Capacity**, and **Description**
6. Add some Workshops to the list

You can be very createive ✨ yourself - we just asked Copilot to generate some ideas: 

| Title                                               | Description                                                                                   | Date           | Capacity |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------|----------------|----------|
| Emotional Intelligence for Leaders                  | Learn to recognize, understand, and manage emotions to enhance leadership effectiveness.       | June 5, 2025   | 30       |
| Effective Negotiation Strategies                    | Develop skills to negotiate confidently, resolve conflicts, and create win-win solutions.      | June 20, 2025  | 25       |
| Cybersecurity Basics: Protecting Company Assets     | Understand cybersecurity fundamentals and best practices to safeguard sensitive data.          | July 10, 2025  | 20       |
| Introduction to Data Visualization with Power BI    | Learn to create impactful dashboards and visualizations using Microsoft Power BI.             | July 25, 2025  | 15       |
| Agile Project Management Essentials                 | Explore Agile principles, Scrum methodology, and practical tools for efficient project delivery.| August 5, 2025 | 35       |
| Public Speaking and Presentation Skills             | Gain confidence and techniques for delivering engaging and persuasive presentations.           | August 20, 2025| 30       |
| Diversity, Equity, and Inclusion in the Workplace   | Build awareness and foster a culture of inclusivity and belonging within your teams.           | September 10, 2025| 40     |
| Conflict Resolution for Teams                       | Develop strategies to manage and resolve workplace conflicts effectively and professionally.    | September 25, 2025| 30     |
| Advanced PowerPoint Design for Professionals        | Create visually compelling and professional presentations using advanced PowerPoint features.   | October 10, 2025| 20     |
| Customer Experience Excellence                      | Understand customer needs and implement strategies to improve satisfaction and loyalty.         | October 25, 2025| 30     |

---

![Workshops list](/assets/espc24-listworkshops.png)

---

## Part B: Creating the **Registrations** List

1. **Create a New List**: Return to the SharePoint site home, select **New** > **List**, and select a blank list

2. **Name the List**: Enter **Registrations** as the list name. Select **Create**

3. **Add Columns to Registrations List**:
   - **Attendee Name**:
     - Select **Add Column** > **Person or Group**
     - Name it **Attendee** and select **Save**
   - **Workshop Title (Lookup Column)**:
     - Select **Add Column** > **Lookup**
     - Name it **Workshop Title**
     - Under "Get information from," select the **Workshops** list
     - Choose **Workshop Title** in the column dropdown
     - Select **Save**
   - **isPresent** > yes/no (default no)

![create a Lookup column](/assets/espc24-createlookup.png)

1. Unrequire and hide the **Title** columnn
    - go to ⚙️ > **List settings** > **Advanced Settings** and set **Allow management of content types?** to `Yes`
    - Select **Ok** (scroll all the way down!)

![allow management of content types](/assets/espc24-allowcontenttypes.png)

   - Select **Item**
  
![SharePoint content types](/assets/espc24-sp-item.png)

   - Select Title

![select title](/assets/espc24-sp-title.png)

- Select **Hidden (Will not appear in forms)**
- Select **OK**
- Select **All Items** > **Add or remove fields**
- Unselect **Title**
- Select **Save**

![remove title](/assets/espc24-remove-title.png)

Now the **Title** column is not visible in the List nor in any form and also its not required to contain information.

## Verify Connection

1. In the **Registrations** list, add a test item to see if the **Workshop Title** dropdown displays data from the **Workshops** list.

![verify link](/assets/espc24-verified.png)

2. **End Result Check**: Confirm that:
   - The **Workshops** list has columns for **Workshop Title**, **Date**, **Capacity**, and **Description**
   - The **Registrations** list has **Attendee** (Person), and **Workshop Title** (lookup column), **isPresent** (yes no)
