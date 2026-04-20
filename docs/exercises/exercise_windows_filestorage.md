---
title: Exercise: Create an SMB Azure file share and connect it to a Windows VM using the Azure portal
---
# Exercise: Using File Storage with Windows VM
## ARCHIVE: see current website <br />https://icer.msu.edu/cloud-computing

## Overview

- Not all versions of Windows can use this.  For much more detail, see the Azure documentation page ["Mount SMB Azure file share on Windows"](https://learn.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-windows)

## Using File Storage with Windows VM step-by-step.
#### First Step: Create a Storage Account

1. We have already set up storage accounts in a previous tutorial. Refer back to the tutorial ([Creating Azure Cloud Storage Accounts](../exercises/exercise_create_storage_account.md)) if you still need to create one, however the one you have currently should work for this tutorial.

#### Second Step: Create an Azure File Share

1. Go to your Storage Account
    * On the homepage, there should be a list of "Resources" in the middle of the page. Click the one with Type listed as **Storage Account**

1. Select File Shares
    * On the left side of the screen there is a menu. Under the "Data Storage" section is the **File Shares** button

1. Add a File Share
    * Towards the top of the screen click the **+ File Share** button

1. File Share Properties
    * Basics
        2. Name the File Share **qsfileshare**
        2. Keep Tier as **Transaction Optimized**
    * Click **Review + Create**

1. Create a new txt file titled **qsTestFile** on your local machine
    * Go to your file folder, and in any directory of your choice - Right Click and select a new .txt file

1. With your file share open in Azure, click **Upload** (on the top middle section of the screen)

1. Upload your created txt file
    * Select **Browse your Files** and navigate to the directory you chose earlier, then attach your txt file

#### Third Step: Deploying a VM

We've created the storage account and the file share with a file in it. We now need to deploy a VM.

1. Create the Resource
    * Expand the left side menu and click **Create a Resource**
    * Under "Popular Azure services" select **Virtual machine**
    
1. Setting the VM Properties
    * Basics
        2. Resource Group: Select the Cloud Computing Fellowship Resource group
        2. Virtual machine name: qsVM
        2. Security Type: Standard
        2. Image: Windows Server 2019 Datacenter - x64 Gen2
        2. Set your Username and Password to something you will remember for logging in to the VM
        2. Select Inbound Ports: HTTP and RDP (3389)
    * Select **Review and Create**
    * Select **Create**
    * When deployment is done, select **Go to Resource**

#### Fourth Step: Connect to Your VM

1. Select **Connect** on the VM properties page

1. Click **Select** on the Native RDP File

1. Download the RDP File
    * On the right side menu select the **Download RDP File** under section 3

1. Open the VM on your local machine
    * Open the downloaded RDP file
    * Select **Connect** on the pop-up
    * Put the username and password that you created in the VM setup (if you are on a windows machine you may need to click "More Choices" before logging in)
    * You may get a certificate warning, you can ignore that

#### Fifth Step: Map the Azure File Share to a Windows Drive

1. In the Azure portal, navigate to your qsfileshare and select **Connect**
1. Click **Show Script** in the right-hand menu pop-up
1. This will display a script in the same menu. Copy and paste this script into your notepad.
1. Go back to your VM
    * Open **Windows Powershell**
    * Paste in the contents of your notepad
    * Press Enter
    * You will see "Credential added successfully" when it works

#### Sixth Step: Working with Snapshots

1. **Create a Share Snapshot**
    - Adding a snapshot in the Azure Portal
        2. In the Azure Portal, navigate to the file share
        2. Select **Snapshots** (located in the left hand side menu)
        2. Select **+ Add a Snapshot** and click Ok
    - In your VM, open the qstestfile.txt and type "This file has been modified". 
    - Save and close the file.
    - Create another snapshot (repeat steps a-c)

1. **Browse a Share Snapshot**
    - On your file share, select **Snapshots**
    - Select the first Snapshot in the list
    - Select **qsTestFile.txt**

1. **Restore from a Snapshot**
    - Ensure you're in the file share Snapshot tab
    - Right click the qsTestFile
    - Select **Restore**
    - Select **Overwrite Original File** and click Ok
    - Open the file in the VM. It should be restored and have no text in it.

1. **Delete a Share Snapshot**
    - On your file share Snapshot list, select the last snapshot in the list
    - Select **Delete**

1. **Use a Share Snapshot in Windows**
    - You can view snapshots from your mounted Azure file share by using the Previous Versions tab
        2. In your VM File Explorer, locate the mounted share. It should be titled **qsfileshare** and have a boxy symbol
        2. Select **qstestfile.txt** and Right Click
        2. Select **Properties** from menu
        2. Select **Previous Versions** - this shows you a list of previous snapshots
        2. Select **Open**

1. **Restore from a Previous Version**
    - In the same screen we were just in, rather than selecting "Open", select "Restore"

#### Seventh Step: Delete the Resources

1. Click on your Resource Group
1. Select everything except the storage account you created in Session 1
1. Select **Delete** NOT "Delete Resource Group" to delete the resources
1. Go to your storage account and delete the fileshare as well