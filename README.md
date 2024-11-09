# Building a Power App with SharePoint Lists and Dataverse

**Runthrough for Luise & Robin:**

**Workshop Goal:** In 6 hours, attendees will

1. Build a basic “Workshop Sign-Up” Power App with SharePoint Lists as the data source
2. Automate the sign-up process using Power Automate (reserved for later in the session)
3. Understand best practices and begin exploring Microsoft Dataverse as an advanced data option

How to instruction for the full day tutorial by [Luise Freese](https://linkedin.com/in/luisefreese) and [Robin Rosengruen](https://www.linkedin.com/in/robinrosengruen/) (Microsoft) at ESPC 24.

WE want to get y ou started with Power Apps and Power Automate and SharePoint and also give you a glimpse on how things work on Dataverse so that you know what to do as you advance

## 1. Workshop Agenda (6 hours)

| Section                                           | Duration | Activity                                                           |
|---------------------------------------------------|----------|--------------------------------------------------------------------|
| 1. Introduction to Power Platform & SharePoint Integration | 30 mins  | Overview, goals, and setup.                                        |
| 2. Building SharePoint Lists                      | 30 mins  | Creating two SharePoint lists and establishing a lookup.           |
| 3. Introduction to Power Apps                     | 30 mins  | Basics of Power Apps Canvas Apps.                                  |
| 4. Building the Power App                         | 1.5 hours | Creating the sign-up app with interactive exercises.               |
| **Break**                                         | 15 mins  |                                                                    |
| 5. Power Automate Placeholder                     | 2 hours   | Reserved for Power Automate integration and exercises.             |
| **Break**                                         | 15 mins  |                                                                    |
| 6. Best Practices & Introduction to Dataverse     | 1 hour    | Optimizing apps, flows, and Dataverse intro.                       |
| 7. Q&A and Recap                                  | 30 mins   | Open floor for questions, recap, and final remarks.                |

---

## Detailed Workshop Content

### 1. Introduction to Power Platform & SharePoint Integration (30 mins)

**Objective:** Introduce the Power Platform, the role of SharePoint Lists, and how Power Apps and Power Automate interact with SharePoint data

1. **Presentation (15 mins)**: Explain Power Platform components (Power Apps, Power Automate) and how they work with SharePoint
2. **Exercise (15 mins)**: Show a sample app and flow; share the final product so attendees know what they’ll build by the end

### 2. Building SharePoint Lists (30 mins)

**Objective:** Set up two SharePoint lists: **Workshops** and **Registrations**. Link them using a lookup column to demonstrate (pseudo) relational data management

1. **Create Lists (15 mins)**:
   - **Workshops List**: Includes columns like **Title**, **Date**, **Capacity**, and **Description**
   - **Registrations List**: Columns include **Attendee Name**, **Email**, and a **Lookup column** for the workshop title

2. **Hands-On Exercise (15 mins)**: Guide attendees through list creation. Verify lists are set up correctly for the app.

### 3. Introduction to Power Apps (30 mins)

**Objective:** Familiarize attendees with the Power Apps Canvas Apps interface and its core components

1. **Presentation (20 mins)**: Walk through the Power Apps Canvas App UI, including screens, galleries, forms, and controls
2. **Demo (10 mins)**: Demonstrate a basic Canvas App to show elements they will use

### 4. Building the Power App (1.5 hours)

**Objective:** Build a sign-up app that allows users to view available workshops, register for a workshop, and store registrations

#### Part A: Setting Up the App (30 mins)

1. **Create New Canvas App**: Set up a blank app connected to SharePoint lists
2. **Add Data Sources**: Link *Workshops* and *Registrations* lists

#### Part B: Display Available Workshops (30 mins)

1. **Create Browse Screen**: Add a gallery to display workshops with Title, Date, and Capacity
2. **Details Screen**: Create a screen that shows workshop details when an item in the gallery is selected

#### Part C: Registration Screen (30 mins)

1. **Create Registration Form**: Add a form for attendees to enter name, email, and select a workshop
2. **Submit Registration**: Add a button to submit the form and save the registration in SharePoint

#### Part D: Testing and Troubleshooting (30 mins)

1. **Test**: Walk attendees through testing their app
2. **Common Issues**: Address common issues, such as data connections and form validation errors

### **Break (15 mins)**

### 5. Power Automate Placeholder (2 hours)

**Objective:** Reserved time for Power Automate integration and hands-on exercises to automate the sign-up process

---

### **Break (15 mins)**

### 6. Best Practices & Introduction to Microsoft Dataverse (1 hour)

**Objective:** Share best practices for Power Apps and Power Automate, with an intro to Dataverse for advanced data scenarios

1. **Best Practices (30 mins)**:
   - Naming conventions for SharePoint columns, flows, and controls
   - Optimizing performance and avoiding delegation issues
   
2. **Introduction to Dataverse (30 mins)**:
   - Explain when to consider Dataverse over SharePoint
   - Briefly demo a Dataverse table to show data relationships and scalability

### 7. Q&A and Recap (30 mins)

**Objective:** Wrap up with a Q&A session to address specific questions and review key points

1. **Open Floor (20 mins)**: Encourage attendees to ask questions about their app or flow
2. **Recap (10 mins)**: Highlight the 3 key takeaways:
   - Building a Power App with SharePoint Lists
   - Automating processes with Power Automate
   - Understanding best practices and when to use Dataverse

---

## Materials and Resources

1. **Slide Decks**: Each section has slides for theoretical explanations and examples
2. **Step-by-Step Guides**: Downloadable guides for each task
3. **Sample Code Snippets**: For Power Apps formulas and Power Automate steps
4. **SharePoint Lists Setup Template**: Pre-configured templates for both lists to save setup time
5. **Q&A Document**: Document FAQs and common issues based on live questions
# PowerApps-ESPC24

## Intro to the Power Platform

## Labs
* Create SharePoint Lists
* Set yourself up for success with a Solution
* Connect your Power App to the SharePoint Lists
* Add and Edit List Items through Power Apps with a Form
* Add Attendees with the Patch command
* Create a Form for Event registration
* Use Power Automate to add your Form entries to SharePoint
* Send a Reminder with Power Automate
* Send Files via Power Automate

## Why you should feel dirty and asahamed about everything that we did in the last 5 hours and how you can create enterprise ready solutions with the Power Platform
