---
title: Storage and data transfer options for VM
hide:
  - toc
---

# Storage and data transfer options for VM
*From [Session #3, Cloud Storage](../../sessions/03_cloud_storage.md)*

## Context

When using a cloud machine or service, a typical workflow is: 

1. **Provision**: create and prepare resources and services: VM, storage, software installation, etc
2. **Stage**: move code, software, and input data to the VM that will do that computations (execution)
3. **Execute**: set the parameters and run the computation which generates output data onto storage
4. **Transfer**: move (aka transfer) the output to the next phase in your workflow, often your own 'local' computer

Input and output may be files but it may also be records in a database. 

Here are 5 popular options for Storage+VM in context, with short description of how to connect and transfer data.   
This a gradient on the amount of work you have to do to alter your software or code from option 1 (no changes) to option 5 (many changes) 


[<img src="../Five_storage_options_for_cloud_vm_to_local_file-date_sharing.drawio.png">](../Five_storage_options_for_cloud_vm_to_local_file-date_sharing.drawio.pdf)


*[Full size PDF](Five_storage_options_for_cloud_vm_to_local_file-date_sharing.drawio.pdf)*


<!-- | Option | Description | complexity |
| 1. Primary Disk | added automatically and any software that can save files can use it with no work on your part | low, don't need to change your code |
| 2. Secondary Data disk | have to add one when creating VM, but can use an existing 'managed disk', works just like primary disk but dedicated to data.  C
| 3. File storage |   | medum, have to connect using command after VM is created   |
| 4. Blob Storage |  | | 
| 5. data storage in a database |  | | 

-->


## Links


### Storage Types

*These links are provided and described in other parts of session 3*

[Azure storage services overview (includes many that are not included in the diagram)](https://learn.microsoft.com/en-us/azure/storage/common/storage-introduction)

- 1 &amp; 2 [Managed Disks](https://learn.microsoft.com/en-us/azure/virtual-machines/managed-disks-overview)
     - You can add data disks when you create a VM - see the [Azure VM creation walk through](../../exercises/azure_vm_walkthrough.md)
     - [About Disks, and how to specify them using the Azure CLI](https://learn.microsoft.com/en-us/azure/virtual-machines/windows/attach-managed-disk-portal)
     - [you can add a data disk to an existing Windows Virtual machine](https://learn.microsoft.com/en-us/azure/virtual-machines/windows/attach-managed-disk-portal)
- 3 [Azure Files](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-introduction)
     - See the [Storage Session Activities](https://msu-icer.github.io/cloudcomputingfellowship/sessions/03_cloud_storage/#activities) for details about connecting file share to a VM
- 4 [Blob Storage](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction)
- 5 [Databases vs Storage](../../topics/storage_vs_databases.md)

Like VM CPUs, there are way to many choices for a VM disk (primary or auxilliary).   Determine the size you need and find the cheapest 'ssd' type you can.   
If you are not concerned about peformance at all, find the cheapest option for 
the size you need. 

### Data Transfer Methods

- **Desktop Application** [Azure Storage Explorer](https://azure.microsoft.com/en-us/products/storage/storage-explorer/) User application for moving data down from and up to Azure cloud storage including disks
- **Command Line Application** [the azcopy utility](https://learn.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10), a command-line utility for moving data to/from your computer to the cloud, or from cloud-to-cloud.   To access Azure Storage accounts
  you must create and use a special URL that includes a Security Key (a "SAS" key in Azure terms).   
- **Python** [Quickstart: Azure Blob Storage client library for Python]( https://learn.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-python?tabs=managed-identity%2Croles-azure-portal%2Csign-in-azure-cli)
- **R** Unfortunately the [R libraries that worked with various Azure services](https://github.com/Azure/AzureR) have not been worked on for several years and there is no guarantee they will work.   [AzureStor](https://github.com/Azure/AzureStor)
- **Database Application** [Azure Data Studio](https://learn.microsoft.com/en-us/azure-data-studio/what-is-azure-data-studio),   a cross-platform application for interacting with databases.  Designed for Micrsoft's branded "SQLServer" but works with many open source databases.  Requires an existing database in the cloud or elsewhere.  There are many open source versions of this kind of database user-interface application: [List of database GUIs](https://www.eversql.com/top-7-mysql-gui-tools-for-windows/)




