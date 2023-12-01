# Identity and Access/Authorization Management : Cloud IAM

### Introduction

A great introduction to IAM from Microsoft Learn: [What is identity and access management (IAM)?](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/introduction-identity-access-management) (for Azure)


"IAM" is how access and authorization are handled for a given cloud resource. 

Robust security controls are a critical element for any organization with a cloud presence, and access management is no exception.

“IAM” refers to a cloud company's collection of services and APIs for managing access and authorization for resources.   If you create a storage account, who has access and how can they access it?     Can a VM read/write/delete from a particular File share?   

Identity management is a huge topic for all of IT, not just for cloud.   Can one server talk to another?  Even apps have identity, especially if
the intention of an app is to access resources, or maybe even create additional resources.    If you write a program that is running in a VM or as part of an
app, can your program create new resources, say a serverless feature like a function, or read from a database?   

The challenge for understanding IAM in cloud is that many of the servers or services you create will also have their own user authentication methods.  
Sometimes a cloud provider may add features to a service (like a database, or Machine learning services, or big data) such that the cloud user (.e.g.
the user account you use to log-in to the portal) can automatically have access to the resource you've created.   That does not have to be true.  
Azure takes this a step further and uses the same identity system used to allow us to access teams and office which means the folks at our U who control 
those kinds of access can also grant acceess to cloud resources.    

### Note about security and IAM

You may think: *"why even bother?  I don't have any thing sensitive in these storage accounts."*     What most people don't realize is that hackers need computing resources (CPU, VM, storage) that are untraceable.   Storage is important to share secrets or contraband from one person or point to another.  A hacker would like to use your storage for it's capability, not for the data inside.   Like a stolen car used to get away from a crime and dumped.   I've seen computers hauled away by the police because someone used it to share illegal images.   Do what you can to keep your cloud resources out of the hands of hackers. 


### Roles

In addition to granting basic access of an account into a resource, we can define the kind of access.  This in security is called a 'role'   You are 'owners' of your 
resource groups meaning you can do almost anything, but we could also grant 'read' access to some of your resources to another person?   This is called
"Role-based Access Control" or RBAC.   Azure defines hundreds of roles for different levels of access to various services.   

### Service Accounts

There is another concept in IAM you will see frequently and that is a "service account" or in Azure terms a "service principle."   If you have a VM 
running a process that yuo need to then access another service (could be storage, but could also be things like data systems, or other services

### Saving Secrets

All cloud vendors have a service for storing passwords.  For example, if we create a database service like Postgres, it will have it's own user id's and 
passwords for connecting and pulling data.   If we ahve an app that needs access, or jupyter notebook, we _could_ use our own IDs, but if we want to 
keep our own ID safe, Azure recommends creating a service account that is actually kind of a computer account.    That was you don't have use your own
account for this VM to access storage, and also it means this VM could be used by multipe people.   

## Use Cases

Storage accounts are a great way to learn about IAM in Azure.   There are several ways to grant access to files inside a storage account 
to anyone but yourself.  We cover some of that in the storage sessions.  

This tutorial is python-specific but quickly lists the 4 types of access and what that means exactly for python code.  
See the [Interfaces](../sessions/04_organization.md) for details about using Python. 

## More Background

This is extra.  I think this is a very well written overview of IAM across different cloud providers.  
It's perhaps too long and detailed for casual users of the cloud but useful if you are learning about Azure but need to someday transfer to another 
provider for your work. 

Comparing AWS, Azure, and Google Cloud IAM services: https://acloudguru.com/blog/engineering/comparing-aws-azure-and-google-cloud-iam-services


