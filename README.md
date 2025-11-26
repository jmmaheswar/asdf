# Table of Contents

## 1. Introduction

This section provides you a step-by-step guide to build a hardware tool inventory app with Mendix. You will learn how to create entities, generate pages, configure navigation, and test your application.

## **2. Prerequisites**

 Before getting started, complete the following prerequisites:

1. Login to your [Mendix account](https://home.mendix.com/login.html) created using the credentials provided. 
2. [Download](https://marketplace.mendix.com/link/studiopro/10.24.11) and [Install](https://docs.mendix.com/refguide/install/) Mendix Studio Pro 10.24.x (LTS).
3. Install and [configure Parallels](https://docs.mendix.com/refguide/using-mendix-studio-pro-on-a-mac/) or install the [10.24.x beta version](https://marketplace.mendix.com/link/studiopro/10.24.11) for MacOS. 

## 3. Accessing the app

To access and edit the TW-2503 app, perform the following steps:

1. Login to your Mendix account with the following credentials:
    
    Work Email Address: [rklqcfxzoubxkitqfo@fxavaj.com](mailto:rklqcfxzoubxkitqfo@fxavaj.com)
    Password: Assignment!2503
    
    ![image.png](ExportBlock-5a4fb65c-495e-4ce8-bcaa-e56f958ac3f6-Part-1/Chadwick’s Hardware Inventory How-tos/5bb70ec2-dd24-4d24-a914-482bd5a32fe9.png)
    
    1. Click on **TW-2503**
        
        ![image.png](ExportBlock-5a4fb65c-495e-4ce8-bcaa-e56f958ac3f6-Part-1/Chadwick’s Hardware Inventory How-tos/5bb70ec2-dd24-4d24-a914-482bd5a32fe9.png)
        
    2. Click **Edit In Studio Pro** to edit and extend the app functionalities.
        
        ![image.png](attachment:fc64afdd-f42a-4790-87d1-8d9b08ab483f:image.png)
        
    3. Select the **TW-2503** app and click **Open in Studio Pro**
        
        ![Screenshot 2025-11-24 at 6.38.13 PM.png](attachment:20c94524-5f4c-4875-9dd9-4feef1e265df:Screenshot_2025-11-24_at_6.38.13_PM.png)
        
    
    You have successfully opened your app on Studio Pro. The app opens with the app homepage titled **Home_Web.**
    
    ![Screenshot 2025-11-24 at 7.04.04 PM.png](attachment:9fe1366f-8a49-4b55-b3e4-b5ae3591e363:Screenshot_2025-11-24_at_7.04.04_PM.png)
    

## 4. Extending the app

### 4.1 Building the homepage

To build and extend the app, perform the following steps:

1. Select and right click to delete all the contents on the Home_Web page.
2. In the right dockable pane, click **Toolbox** and click **Widgets.** 
3. From the **Structure** dropdown, drag and drop **Containers** to the homepage**.**   

![Screenshot 2025-11-24 at 11.17.21 PM.png](attachment:75187ab8-6bfd-4bf6-baa9-d95951b57666:Screenshot_2025-11-24_at_11.17.21_PM.png)

1. From the **Text** dropdown, drag and drop the **Page Title** . Click the **Topbar** and rename it to Chadwick’s Hardware Inventory.
    
    ![Screenshot 2025-11-24 at 11.41.35 PM.png](attachment:b12f8569-a1eb-4987-be1e-f144e0fe81a7:Screenshot_2025-11-24_at_11.41.35_PM.png)
    
2. Open the **Cards** dropdown, then drag and drop a **Card Action** block onto the homepage. Rename the card to Tools.
    
    ![Screenshot 2025-11-24 at 11.43.38 PM.png](attachment:614eebc0-bf31-4e78-9a1b-362297a55eb4:Screenshot_2025-11-24_at_11.43.38_PM.png)
    
3. Click **Properties** and navigate to **Styling**. Adjust the card spacing to your preference. 
    
    ![Screenshot 2025-11-24 at 11.47.41 PM.png](attachment:03710562-eb33-4e07-bcff-527c04696593:Screenshot_2025-11-24_at_11.47.41_PM.png)
    
4. Click the **button** icon and configure the following properties:
    1. Icon: add-circle
    2. Render mode: Button
    3. Button style: Primary
5. Style the button with these settings:
    1. Spacing: Margin Left, Right: Left
    2. Size: Large
    3. Border: Enabled
    
    ![Screenshot 2025-11-25 at 12.22.26 AM.png](attachment:ee1d059d-73fb-4168-8215-e76726181226:Screenshot_2025-11-25_at_12.22.26_AM.png)
    
6. To preview the homepage, click **Run Locally** and click **View App.** The homepage should look like this:
    
    ![Screenshot 2025-11-25 at 1.24.38 AM.png](attachment:d213af17-3f7f-4747-98f1-e187fb09cfec:Screenshot_2025-11-25_at_1.24.38_AM.png)
    

### 4.2 Building the Tools page

1. In the App Explorer, expand the **MyFirstModule** dropdown and click **Domain Model.**
    
    ![Screenshot 2025-11-26 at 7.02.12 AM.png](attachment:ed811f86-bc4f-44ad-8f71-e4354bf6921d:Screenshot_2025-11-26_at_7.02.12_AM.png)
    
2. Drag a new **Entity** from the **Toolbox** into the domain model. Alternatively, right-click anywhere in the Domain Model and select **Add entity.** You have created a persistable entity, all the tool information will be stored in a database.
    
    ![Screenshot 2025-11-26 at 7.09.51 AM.png](attachment:fd365c4a-7bdf-463e-ba3e-b82f2dd0aaeb:Screenshot_2025-11-26_at_7.09.51_AM.png)
    
3. Double click the entity to open the properties. Name the entity Tool. 
    
    ![Screenshot 2025-11-26 at 7.12.22 AM.png](attachment:1a7cd51b-91e5-40a2-84ea-6d44c1a78334:Screenshot_2025-11-26_at_7.12.22_AM.png)
    

 4. To create a new attribute, click **New.** This will open a dialog box.

![Screenshot 2025-11-26 at 7.25.35 AM.png](attachment:e94d3d9e-0b38-4d79-8956-79390798e36d:Screenshot_2025-11-26_at_7.25.35_AM.png)

 5. Create four attributes.

| **Name** | **Type** |
| --- | --- |
| Name | String |
| Code | String |
| Quantity | Integer |
| Price | Decimal |

<aside>
📖

There are four types of entities. Learn more about entities [here](https://docs.mendix.com/refguide/entities/#entity-types).

</aside>

The Tool entity property dialog will look like this: ****

![Screenshot 2025-11-26 at 7.36.08 AM.png](attachment:78861c72-a749-43f4-bd01-f31ed115ce99:Screenshot_2025-11-26_at_7.36.08_AM.png)

1. Click **OK.**
    
    ![Screenshot 2025-11-26 at 7.36.49 AM.png](attachment:b8d427c2-ba49-4363-9355-c6fb25feea2b:Screenshot_2025-11-26_at_7.36.49_AM.png)
    

You have now created an entity. 

To create the tools overview and details page, perform the following:

<aside>
📖

**Note:** There are multiple ways to generate overview pages. For more information refer [Creating Overview Pages](https://docs.mendix.com/refguide10/view-entity-overview-pages/). 

</aside>

1. Right click the Tool entity and click **Generate overview pages** and click **OK.**
    
    ![Screenshot 2025-11-26 at 7.53.20 AM.png](attachment:4fd07629-3a58-4996-a08e-64a2e2503f58:Screenshot_2025-11-26_at_7.53.20_AM.png)
    
2. Click the **OverviewPages** folder to view the pages.
    
    ![Screenshot 2025-11-26 at 8.04.44 AM.png](attachment:6621a531-b1fa-424d-9e51-3aaea3154af2:Screenshot_2025-11-26_at_8.04.44_AM.png)
    
3. Click the **Tool_Overview** page and click the **New Tool** button to adjust the spacing in the **Properties.** 
    
    ![Screenshot 2025-11-26 at 8.13.51 AM.png](attachment:5ed6c83a-995a-4c13-84be-0b6b4a1fd5bf:Screenshot_2025-11-26_at_8.13.51_AM.png)
    
4. Double click the **New Tool** button to open the edit action button properties and rename the **Caption** to Add a new tool.
    
    ![Screenshot 2025-11-26 at 8.17.02 AM.png](attachment:6d1bebda-9803-4a75-843c-4df3f7762849:Screenshot_2025-11-26_at_8.17.02_AM.png)
    
5. Double click the Tool text and rename it to **Tools Overview.**
    
    ![Screenshot 2025-11-26 at 8.46.23 AM.png](attachment:246984a5-e201-49dd-b5fb-387e92cb0b49:Screenshot_2025-11-26_at_8.46.23_AM.png)
    
6. Select all the text filters and click **Delete.**
    
    ![Screenshot 2025-11-26 at 9.00.21 AM.png](attachment:ca06e38f-2259-477c-8c3d-608f9ba44ed1:Screenshot_2025-11-26_at_9.00.21_AM.png)
    
7. In the **App Explorer,** click **Tool_NewEdit.**
    
    ![Screenshot 2025-11-26 at 9.12.14 AM.png](attachment:10005015-20df-46c2-a692-8e345c808c82:Screenshot_2025-11-26_at_9.12.14_AM.png)
    
8. Click each attribute to open the properties dialog box and set the **Validation Type** to **Required.**
    
    ![Screenshot 2025-11-26 at 10.51.24 AM.png](attachment:644efad2-e4ba-42d5-9ab8-fb7d9bbf00c7:Screenshot_2025-11-26_at_10.51.24_AM.png)
    

You have now created the three pages required. To create navigation between the pages, perform the following steps:

1. Clic **Navigation** in App Explorer.
    
    ![Screenshot 2025-11-26 at 11.02.56 AM.png](attachment:d1eab38a-6c43-4428-94b4-d12bf9b41f85:Screenshot_2025-11-26_at_11.02.56_AM.png)
    
2. Click **New Item** from the **Menu** section.
    
    ![Screenshot 2025-11-26 at 11.06.49 AM.png](attachment:8f6e1142-1dcb-42e9-b706-880a804ccb35:Screenshot_2025-11-26_at_11.06.49_AM.png)
    
3. Set the **Caption** to Navigation and set the **Icon** to **compass-directions** and click **Select.**
    
    ![Screenshot 2025-11-26 at 11.16.19 AM.png](attachment:4d122f88-6718-46f2-9016-0e0d283d132c:Screenshot_2025-11-26_at_11.16.19_AM.png)
    
4. Set **On click** to **Show a page.** From the **Select a web page** dialog box, click **Home_Web** and click **Select.**
    
    ![Screenshot 2025-11-26 at 11.21.42 AM.png](attachment:255883f9-ea03-44bc-ac34-03218ae42682:Screenshot_2025-11-26_at_11.21.42_AM.png)
    

In the Home Page, perform the following steps to configure the card action button to open the **OverviewPages:**

1. Double click on the button to open the **Edit Action Button** dialog box. Select **Show a page** in the **On Click** option under the **Events** section.
    
    ![Screenshot 2025-11-26 at 11.36.08 AM.png](attachment:00ee2284-4c70-4d23-9a6a-4b1f1ce5dd49:Screenshot_2025-11-26_at_11.36.08_AM.png)
    

1. Expand **OverviewPage** and select **Tool_Overview** and click **Select.**
    
    ![Screenshot 2025-11-26 at 11.40.31 AM.png](attachment:c20ff3f9-2024-4cc6-966e-fba2f09645e9:Screenshot_2025-11-26_at_11.40.31_AM.png)
    

You have successfully configured the button to open the Tools page.

## 5. Testing the app

To test the app, follow the instructions given below:

1. Click the **Run** **Locally** icon on the **Run Menu.**
    
    ![Screenshot 2025-11-26 at 12.17.24 PM.png](attachment:9f75ed9a-97f0-49e8-a321-1820e407ea96:Screenshot_2025-11-26_at_12.17.24_PM.png)
    
2. Once the app is running, click **View App.** The app is deployed locally on your machine. 
    
    ![Screenshot 2025-11-26 at 12.24.30 PM.png](attachment:ded5a0cc-3426-420b-b220-4d751e21d531:Screenshot_2025-11-26_at_12.24.30_PM.png)
    

## 6. Adding sample data

To add sample data to your app, perform the following steps:

1. Click the **Add** button.
    
    ![Screenshot 2025-11-26 at 12.45.06 PM.png](attachment:ce1ef696-54eb-43cb-86b7-73d7cd6ac426:Screenshot_2025-11-26_at_12.45.06_PM.png)
    
2. Click **Add New Tool.**
    
    ![Screenshot 2025-11-26 at 12.46.28 PM.png](attachment:6382419b-a41f-47dc-8c95-d9b09d80d71f:Screenshot_2025-11-26_at_12.46.28_PM.png)
    
3. Enter the Name, Code, Quantity and Price of the tool and click **Save.**
    
    ![Screenshot 2025-11-26 at 12.47.57 PM.png](attachment:d235658c-f782-42ff-9dbc-e5d616378dee:Screenshot_2025-11-26_at_12.47.57_PM.png)
    

A new tool has been added to the database.

![Screenshot 2025-11-26 at 12.48.26 PM.png](attachment:909708bf-a2c6-4621-bf58-94320a14dfc7:Screenshot_2025-11-26_at_12.48.26_PM.png)

The video below demonstrates the complete workflow of the hardware inventory app, including navigation, adding tools, and viewing the tools overview:

[Hardware Inventory.mp4](attachment:a4d9a23e-b668-4bcf-b7f5-204ddea7fa9d:Hardware_Inventory.mp4)

## 7. Publishing the app

1. Click **Publish.**
    
    ![Screenshot 2025-11-26 at 1.01.08 PM.png](attachment:f747d214-6c60-4570-948a-af40c5014367:Screenshot_2025-11-26_at_1.01.08_PM.png)
    
2. Once the app is published, open the Mendix portal and click **View App.** It will redirect you to the web app.
    
    ![Screenshot 2025-11-26 at 1.07.22 PM.png](attachment:55a556bd-33e0-4ef3-b7ae-3c53cf773df2:Screenshot_2025-11-26_at_1.07.22_PM.png)
    

Congratulations! You successfully built a hardware inventory web app. Well done!

![Screenshot 2025-11-26 at 1.09.17 PM.png](attachment:e8135a06-467e-4dd3-a055-89227c2dd572:Screenshot_2025-11-26_at_1.09.17_PM.png)
