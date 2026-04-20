---
title: 4 - Cloud Services Organization
---

# Session 4: Cloud Services Organization
## ARCHIVE: see current website <br />https://icer.msu.edu/cloud-computing

![disorganized wiring](http://www.itrw.net/wp-content/uploads/2016/06/server_spaghetti_1.jpg)


## Goals
This is a collection of topics about the organizational aspects of cloud computing so may seem unfocused but each topic is important
for successful application of cloud computing.   We hope to provide you with the following understanding of: 

 - what options for interacting with cloud services
 - Understand difference between the cloud manager and resource you've created
 - Know how to use program to automate the creation and deletion of cloud resources 
 - How to find basic cost estimates
 - what are the "service levels" and the related responsibilities for different kinds of cloud resources, and how does that help you choose a service
 

## Introduction

We might think of using cloud computing in 3 areas: 

1. using the resources (which is our real goal), 
2. definining and creating these resources, and 
3. managing them.  

We may need a virtual machine to run our program to calculate or analyze our data, but we need to determine the properties of that virtual machine and create it first.  Surrounding all of that is how we interact with the cloud service to do that, how we estimate and observe the costs, manage and identify all the other components a cloud VM needs, and  make it as secure as possible.   

I'm lumping all of these last pieces into 'managing' cloud resources.  It may be the most boring of all the topics.   The concepts may cover any resource you create in the cloud, and in general apply to all cloud service providers.  However the details of _how_ you do it are very specific to each cloud vendor.   In fact the methods may be convoluted or less than straightforward, so there are many companies that provide additional tools just to manage cloud resources in a more consistent or easier way than the cloud providers allow you


## Interfaces to Cloud Services

In session one we talked about the client/server model of computing which is so ubiquotous is seems like the _only_ model of computing.  

The core of the cloud model is that "everything has an API" or Application Programming Interface:  the commands that can be used for code-to-code interaction. 

Note the "Interface" we are discussing here is for interacting with Azure to manage resources. 
Once created, the resources themselves may have their OWN interface, which is highly dependent on the resource (for example, the 
interface to a Microsoft Windows virtual machine is the remote desktop client and then of course Windows itself)

#### Interfaces Reading: 

- [Interfacing with Cloud Services](../topics/intro_to_cloud_interfaces.md)

#### Interfaces Activity: 

- Introduction the the Cloud Shell https://docs.microsoft.com/en-us/azure/cloud-shell/overview
- [Create a Linux virtual machine with the Azure Command Line Interface ( CLI) ](../exercises/exercise_vm_via_cli.md)

## Other topics: 

- [Moving Data in the cloud](../topics/moving_data/moving_data_in_cloud.md)
- [Staying Organized in Azure](../topics/staying_organized_in_azure.md)
- [Costs](../topics/azure_cloud_cost_basics.md)
- [Monitoring](../topics/monitoring_in_azure.md)
- [Service Level Model of cloud computing](../topics/service_level_model_of_cloud.md)


