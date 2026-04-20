# What is a Server?   An Exercise
## ARCHIVE: see current website <br />https://icer.msu.edu/cloud-computing

The client/server model of computing is so ubiquitous that we don't think of it is one of several models to choose from.   
The internet and the web uses this client server model.  Your web browser is the client, and someone running a website is using a server. 

Client/Server computing is at the core of cloud computing.    Almost everything we build in the cloud is a server.   It's because it's a server that we can access it and control it remotely.   But what is a server?

A server has these components: 

- access to the network
- the network security has given the ability to connect to the computer
- a computer 
   - has networking in it (all modern computers and also virtual machines )
   - runs an operating system that is configured to use the network (all modern operating systems Windows, Linux, Mac)
- a program installed and running on that computer that listens for requests from the network, and returns responses over the network

when you install a program on your computer of course you access it directly.  But can you install a program on a cloud computer and access it remotely?   

What kinds of programs are servers?  that is not just an desktop application?
  - Python Notebook Jupyter server
  - Rstudio has a server version of Rstudio that runs like a website.  this is very confusing becuase they look identical!
  - A web-based GIS server to be able to work with maps remotely
  - A remote desktop server, that we have used with the remote desktop client.  The Azure DSVM automatically installs this
  - A database server to give us data when we ask of it
  - a web server that serves html files that your browser can display


Let's launch a VM that runs the Jupyter program that is a webserver that allows us to use Python remotely on a computer.    

The vast majority of servers on the internet today run Linux.   There are Windows servers but they are for a pretty different system for IT Centers so we won't cover those here.    

The Azure data science virtual machine template is not made for server, but there are some servers on it, so we wil use it. 

Follow these instructions to create and launch a new Virtual machine running linux.   I strongly recommend the following changes

In step 5: 
1. when creating a user name, use all lower case.   You may want to use your netid
2. Use password for 'authentication type' as the instructions say (ssh is more secure but for this exercise password is faster).  Don't use your netid password!! I actually write this password down to remember
3. Before creating, go the 'tags' section and add at least one tag as we've discussed to help you find all of the related resources to delete them.  

[Azure Quickstart: Set up the Data Science Virtual Machine for Linux (Ubuntu)]https://learn.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/dsvm-ubuntu-intro?view=azureml-api-2

Skip down the section [JupyterHub and JupyterLab](https://learn.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/dsvm-ubuntu-intro?view=azureml-api-2#jupyterhub-and-jupyterlab).   It talks about copying the IP address from the portal, which you need for the next step.   My example, the IP address is 
52.180.147.168

*aside: For those of you who may be interested in command line, you can get also the ip adress using `az vm show -d -g <resourceGroupName> -n <vmName> --query publicIps -o tsv` replacing the resource group name and vm name with your own.*

Your VM is running a jupyer server that is a web-based server.   On your laptop, open your the IP address above like this 

**Change the numbers to match your VM**

https://52.180.147.168:8000

You are not running a notebook server!  But you have to keep it up to date and secure!  what are your options? See info about [Databricks Spark Notebooks](../sessions/05_big_data.md)

