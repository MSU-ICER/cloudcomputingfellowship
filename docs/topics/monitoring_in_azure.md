# Monitoring Cloud Resources in Azure
## ARCHIVE: see current website <br />https://icer.msu.edu/cloud-computing

You want to keep an eye on the resources you create: how healthy are they, are they performing as expected?  Is there some problem that makes them slow or unresponsive?  This is especially true of servers, created by IT staff, that others are using that need to stay up and running.    For us as researchers creating resources to do our calculations, we want to know how long it's taking and hence how much will it cost?  Do we need to add more power to get it to work?   

This is an esoteric topic and is really specific to each type of service, but it's something to consider as 1) you may need to engage in a resource outside of the azure portal (e.g. in a VM, log-in and check the performance with standard tools like 'top' in Linux and the task manger in Windows) 2) create (and pay for!) yet another cloud resource for collective and 'managed' monitoring.     

Why use cloud monitoring at all?  If you were running a bunch of your own computers in your lab, you would just sit down and check on them using tools the operating system provided.  In many systems you open and read the 'logs' or text files with a stream of the events and times they occured.  

Machines in the cloud provide new challenges.  An obvious one is to be able to see statistics for many resources at once.   How then does Azure collect data from each machine into central place and then let you browse it?    A second challenge is, what happens to that information for a virtual machine that has crashed and is unresponsive, or has been intentionally turned off and deleted?   

### Monitoring Examples

For Azure virtual machines, Azure offers ["Azure Monitor"](https://learn.microsoft.com/en-us/azure/azure-monitor/vm/monitor-virtual-machine).   Using it is completely optional and I don't have activities related to this service.   If for your project you are working with a group of VM's, you are interested in performance, or you need performance information because your analysis is not completing then I would investigate this service. 

