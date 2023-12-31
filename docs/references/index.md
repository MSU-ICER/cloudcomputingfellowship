# Cloud Computing References and Links to Azure Documentation
## Cloud Computing for Research

**"Cloud Computing for Science and Engineering", Foster and Gannon**  

- [Chapter 1: Orienting in the cloud universe](https://s3.us-east-2.amazonaws.com/a-book/Orienting.html) 
     ( *[Alternative link to publisher preview chapter](https://mitpress.ublish.com/ereader/239/?preview#page/1)*  )


[Using Cloud Computing for Academic Research](../references/DRAFT_cloud_computing_for_academic_research_parvizi_2021.pdf), Mahmoud Parvizi, unpublished draft, 2021.   

Several additional resources for learning about cloud from Cloudbank, a west-coast consortium to help researchers use cloud computing:  https://cloudbank-project.github.io/cb-resources/

Very in-depth case study of cloud for simulations (climate models): \
[Cloud Computing for Climate Modelling: Evaluation, Challenges and Benefits](https://www.mdpi.com/2073-431X/9/2/52). Montes, D., *et al*. *Computers* 2020, 9(2), 52; https://doi.org/10.3390/computers9020052(2020).
## General Cloud Computing Interest

Historical Note [Who Coined 'Cloud Computing'?](https://www.technologyreview.com/2011/10/31/257406/who-coined-cloud-computing/) by Antonio Regalado, October 2011, MIT Technology Review

Intro to Cloud Computing from Microsoft which is primarily for IT people responsible for spending money and maintaining IT Infrastructure: [MS Training Describe cloud computing](https://learn.microsoft.com/en-us/training/modules/describe-cloud-compute/)

## Azure Resources

### General Azure References

Main Azure Documentation : https://docs.microsoft.com/en-us/azure/ 

List of All Azure Services : https://portal.azure.com/#allservices 

Azure Tips and Tricks : https://microsoft.github.io/AzureTipsAndTricks/

Azure Portal "How to" series - focused on using the Azure portal to do several different things.  This is mostly about the services themselves, not the portal, and many topics do not apply to us (e.g. Azure Arc) but there are some very useful videos : https://youtube.com/playlist?list=PLLasX02E8BPBKgXP4oflOL29TtqTzwhxR

These look like really good intros to Azure, but requires a time investment.  The examples are not really research computing examples but may be valuable learning examples.  Most of these lessons were taken from other 'learning paths' and are still oriented towards IT professionals

**Microsoft Learn**: 
  - [Azure for Researchers part 1: Introduction to Cloud Computing](https://docs.microsoft.com/en-us/learn/paths/researcher-introduction-to-cloud-computing/)
  - [Azure for Researchers part 2: Cloud Security and Cost Management](https://docs.microsoft.com/en-us/learn/paths/researcher-cloud-security-cost-management/?WT.mc_ID=academic-31612-leestott)
  

### Azure Books available to the MSU Community via the Library

[Search for Microsoft Azure, ordered by date](https://catalog.lib.msu.edu/Search/Results?sort=year&join=AND&type0%5B%5D=Title&lookfor0%5B%5D=microsoft+azure&bool0%5B%5D=OR&illustration=-1&limit=20&daterange%5B%5D=publishDate&publishDatefrom=&publishDateto=&dfApplied=1&filter%5B%5D=%7Einstitution%3A%22Michigan+State+University%22)

[Microsoft Azure Functions: Developing Serverless Solutions](https://catalog.lib.msu.edu/Record/hlm.ebs100615608e?sid=2958161)
Trevoir Williams, Packt Publishing 2022 

[Practical Azure SQL Database for Modern Developers](https://catalog.lib.msu.edu/Record/hlm.ebs27028684e?sid=2958161)
Davide Mauri, Silvano Coriani, Anna Hoffman, Sanjay Mishra, Jovan Popovic  Apress 2021. 

[Planning, Deploying, and Managing the Cloud](https://catalog.lib.msu.edu/Record/hlm.ebs26363669e?sid=2958161)
Julian Soh, Marshall Copeland, Anthony Puca, Micheleen Harris. Apress 2020.

### Interface: Azure Portal

Azure Portal Documentation :  https://docs.microsoft.com/en-us/azure/azure-portal/ 

Microsoft Azure Hierarchy: [Organize your Azure resources effectively](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-setup-guide/organize-resources?tabs=AzureManagementGroupsAndHierarchy)


Re-organize your portal view by creating a new dashboard (optional) : https://docs.microsoft.com/en-us/azure/azure-portal/azure-portal-dashboards

Azure portal productivity Tips : https://microsoft.github.io/AzureTipsAndTricks/blog/tip329.html#azure-portal-productivity-tips


https://microsoft.github.io/AzureTipsAndTricks/blog/tip329.html

## Azure Interface: Azure Command Line

Command-line progamming of Cloud Services

 * Azure PowerShell (Windows) https://docs.microsoft.com/en-us/powershell/azure/ 

    * Introduction to PowerShell : https://docs.microsoft.com/en-us/powershell/azure/get-started-azureps?view=azps-3.0.0 

 * Azure Command Line Interface (CLI) (MacOS, Linux): https://docs.microsoft.com/en-us/cli/azure 

    * Introduction to Azure CLI https://docs.microsoft.com/en-us/cli/azure/get-started-with-azure-cli?view=azure-cli-latest 

 * Hybrid inferface: using the CLI inside the Azure Portal
   You can install and use the `az` CLI program on your own computer, but Azure also has a way you can use the CLI without installing anything, with a cloud-based terminal interface called the "cloud shell."   For an overview see https://docs.microsoft.com/en-us/azure/cloud-shell/overview and for a great 'quickstart' see https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart for a quick tutorial for how to use it.   
   In the quickstart, the first example shows you how to create a resource group using the CLI in the cloudshell.  If you don't have permissions to create a new resource group, skip to the next example ("Create a Linux VM") and put your own resource group in the command for the `-g` parameter and perhaps use a very unique name for the VM parameter. 


 
### Azure Storage

Create a Storage Account: 

https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account 

Azure Storage Explorer: https://azure.microsoft.com/en-us/features/storage-explorer/ 

Blob Storage Documentation: https://docs.microsoft.com/en-us/azure/storage/blobs/  

Create and Manage a Storage Account: 
https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account 

 
Using the CLI with Storage Reference:
https://docs.microsoft.com/en-us/cli/azure/storage/account 


Using PowerShell Storage Reference:
https://docs.microsoft.com/en-us/powershell/module/azure.storage 

Create blob storage with CLI:

https://docs.microsoft.com/en-us/azure/storage/common/storage-azure-cli 


Create blob storage with PowerShell:

https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-powershell 
 

### Compute 

Overview of Compute Options: https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-overview 

Choosing an Azure Compute Service (Decision Tree):  https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-decision-tree

 
### Interface: ARM templates


Azure Resource Manager Templates are JSON-formatted configuration files that dictate which resources to create.   

*See also information on 'Bicep', which is Azure's sipmlified (but still complex) template language to replace the ARM templates*


Overview of ARM templates:  https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/overview

explore quick start ARM templates (web): https://azure.microsoft.com/en-us/resources/templates/

explore quick start ARM templates (github): https://github.com/Azure/AzureStack-QuickStart-Templates

  * many of these github repositories include a "deploy to Azure" button that will run the template via the portal and create resources. 


### R and Azure 

https://blog.revolutionanalytics.com/2018/12/azurestor.html 

https://cloudblogs.microsoft.com/opensource/2019/07/01/azurer-available-create-manage-monitor-azure-services-r/ 

https://docs.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/r-developers-guide 

https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/r-packages-supported-by-azure-machine-learning 

https://github.com/Azure/AzureContainers 

https://github.com/Azure/AzureR 

https://github.com/Azure/AzureRMR 

<!-- check that ml studio is still supported 
https://www.r-bloggers.com/how-to-evaluate-r-models-in-azure-machine-learning-studio/ -->

 

### Python and Azure 

https://azure.microsoft.com/en-us/develop/python/ 

https://docs.microsoft.com/en-us/azure/python/ 

https://github.com/Azure/azure-sdk-for-python 

https://github.com/Azure/azure-storage-python 

https://azure.github.io/azure-sdk/releases/latest/all/python.html (Note that pypi.org/project/azure/  is deprecated/obsolete if you find that via google)


### MATLAB and Azure 

https://blogs.msdn.microsoft.com/uk_faculty_connection/2017/06/29/running-matlab-on-azure-provision-a-matlab-distributed-computing-server-using-azure-vms/ 

https://github.com/mathworks-ref-arch/matlab-on-azure 

https://www.itcentralstation.com/products/comparisons/mathworks-matlab_vs_microsoft-azure-machine-learning-studio 

https://www.mathworks.com/solutions/cloud.html 


### Microsoft Azure Cosmos DB

CosmosDB is a very large scale data system that can act like other database systems including SQL, MongoDB (a popular no-sql database), and others.  
It's advantage is that it can handle extremely large data sets  (65tB) but is easy to get started.    Google and AWS have similar offereings ( "BigQuery" and "Aurora" respectively). 

If your data is not large, consider using SQL data systems which are also very widely used (and can be used on your own computer)

Intro: https://docs.microsoft.com/en-us/azure/cosmos-db/introduction

It can be free to use, but you have to turn that on when creating the service for your account: https://docs.microsoft.com/en-us/azure/cosmos-db/free-tier

You can run a notebook inside the databaase to queery data with python : 

  * Notebook Description: https://docs.microsoft.com/en-us/azure/cosmos-db/cosmosdb-jupyter-notebooks 
  * Service announcement: https://azure.microsoft.com/en-us/blog/analyze-and-visualize-your-data-with-azure-cosmos-db-notebooks/
  * Video: https://www.youtube.com/watch?v=OrnZMkP5Eq4&list=PLLasX02E8BPBKgXP4oflOL29TtqTzwhxR&index=7


## Cloud Architecture

This section has resources for advanced to intermediate cloud users who are interested in much more details that most researchers will ever need, and are really geared for IT staff.  However, sometimes to find insight into how to approach your problem (especially for cloud timing ooptimazation projects) these may have useful sections. 

**Microsoft Azure Infrastructure Services for Architects** by John Savill, Oct 2019, available from the MSU Library : http://catalog.lib.msu.edu/record=b13538669~S39

Azure has changed since 2019 but may still be relevant