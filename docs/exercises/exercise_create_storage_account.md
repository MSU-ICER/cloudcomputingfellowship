---
title: Create a Storage Account
---

# Creating a "Storage Account" with the Azure Portal
## ARCHIVE: see current website <br />https://icer.msu.edu/cloud-computing

![old post office boxes](../img/old_po_boxes_tim-evans-Uf-c4u1usFQ-unsplash.jpg)

**(From: [Session 1 - Introduction](../sessions/01_introduction.md))**

This is a good activity to explore the Azure portal by creating a new resource.  Storage accounts do not accrue much cost until you fill them up with data.  Please review the exercise [Azure Portal Walk-through](./azure_portal_walkthrough.md) if you haven't. 

We have not talked about Cloud storage, however you don't need to know about Cloud storage to complete this tutorial.  This is simply an exercise to see how you would create something using the Azure portal, and Cloud storage is a benign (and very inexpensive) resource to use an example.  

Note that a "storage account" is not the same as "disk" you will see when you create a virtual machine.  We will discuss the difference in detail in the session on storage. 

## Requirements:

  * An Azure Account with valid subscription
  * A Resource group

*All members of the current Cloud Computing Fellowship cohort have these things.*

## Creating a storage account step-by-step.
#### First Step: Accessing a Storage Account Template.

1. Log-in to the Azure portal if you have not already. (https://portal.azure.com)
1. Click the menu (top left, three horizontal bars).
1. Select **Home** from the menu. (This is to ensure we all have the same view)
1. Select **Create a Resource** in the upper left screen under Azure Services. 
   <i>Yes we could have click "storage accounts" instead but we want to demonstrate how to use the next screen...</i> 
    * Note:  The current screen is where you can create almost any service Azure offers, and additional services created by third-parties or companies that are not Microsoft.   When you are starting, ensure you are creating a service from Microsoft (we'll show you how in the next step)
1. In the lower search bar (labeled *Search services and marketplace*), type **Storage account**   Note that "storage" alone lists many other kinds of resources. 
1. You will see a list of several services. Select the first one labeled **Storage account** (icon looks like a green spreadsheet).   
    * Note: The description of the service will say the provider, which should be Microsoft, if not go back using the back button and search for storage account again.
1. Click **Create** under *Storage account*.

#### Second Step: Setting up the Storage Account.
Note: The Azure resource creation screens mostly work like this: there are so many settings Azure has split these up into groups which are listed horizontally across the top.   You may work though these by clicking each group, OR finish a screen, and click "Next.." button on the bottom of the form.   At any time you may click "Review and Create" and if you've missed some crucial setting, Azure will not let you create the resource without fixing it.  We will go page-by-page for these settings

1. **Basics**: 
    2. **Subscription**: Cloud Computing Fellowship
    2. **Resource Group**: Select your resource group provided to you.
    2. **Storage Account Name:**  
        * some resources have restrictions on naming.  Next to storage account is an "i" in a circle that has more information.  For storage accounts, they must be unique in region, and only numbers and  lowercase letters are allowed.  I don't know if Non-US letters are allowed (e.g.箱)
        * use your MSU ID (NetID) when you name things so help me keep track and also to help find a name that is unique.  So, replace "NETID" with your MSU NetID here:  "stNETIDccf22"   e.g. stbillspatccf22
        * If you are repeating this tutorial, simply add a "2" or "B" e.g. "stbillspatccf22B"  We can delete these experiments later.  
        
    2. **Region (Location)**:  Change this location to US Central.  Click in here to see the options. In practice, pick the region that is closest to you or where your data will be moving to (e.g. North Central US for MSU) but there are other considerations. 
    2. **Performance**: Standard
    2. **Redundancy**: change from GeoRedundant to "Locally Redundant" (LRS).  We won't see a difference, and LRS is cheaper. Beneath that, leave the "make read access...." box checked. 
    2. Click **next...Advanced**

1. **Advanced**: 
    * Leave all of these settings as-is. Click **next...** 
1. **Networking**: 
    * Leave all of these settings as-is. Click **next...**
1. **Data Protection**: 
    * Leave all of these settings as is.  These settings allow you to recover files up to 7 days after deleting or over-writing. click **next...**
1. **Encryption**: 
    * Leave all of these settings as is.  click **next...**
1. **Tags:**
    * Tags are optional but eventually highly recommended.  For now you can leave them blank.  
1. **Review and create**
    * review gives you a chance to double check your settings before committing
    * click **Create**

#### Third Step: Deploying the Storage Account

1. **Deployment**
    - Azure calls the process of creating cloud resources a "deployment."   This term comes from the software engineering process of first "building" an application or utility (or "compiling" which is often not necessary for scripting languages like Python or R) and then moving that application onto the IT servers that make it available.  On your own computer you download software that is already "built" (e.g. MS Word) and installing it is a form of deployment.   
    - Deployment takes a while as the Azure Resource Manager takes your order and runs the code to generate the cloud resource you've described. 
    - You may leave this page and the deployment will continue in the background.   
1. **Finish and Review**
    - When the deployment is complete, in the top bar of the Azure portal you'll see a number badge on the  "Notification" icon indicating the number of messages you have (probably just 1).   Click on the Notifications icon to show this message.   
    - the message should be something like: 
            Deployment succeeded
            Deployment 'resourcename_12345678901234' to resource group 'group name' was successful.
    - "Go to Resource" button will open the Portal page with options for the resource
    - "Pin to Dashboard" will create a  new tile that is a shortcut to this resource on your dashboard for easy access.   If you want to experiment with dashboard arranging then it's ok to click this and easy to remove later from your Portal Dashboard (it will be added to the bottom)

1.  **Examine Resource (storage)**
    - We have not talked about how storage works but the storage resource page is a good example to learn how the Portal is organized.  
    -  If you didn't already click "go to resource", open the top menu and click "home"
    - the Portal "Home" has a list of "recent resources" and this should be at the top.  
    