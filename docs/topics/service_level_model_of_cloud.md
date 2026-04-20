# Service Level Model of Cloud
## ARCHIVE: see current website <br />https://icer.msu.edu/cloud-computing

As you've discovered, Cloud Computing Services are a complex set of hundreds of offering and of course we humans like to put 
things into an organizational framework.   

The [NIST definition of cloud computing](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-145.pdf) defines what
cloud computing is, but also defines the so-called service models.   The convention is to take some aspect of IT, and add the suffix 
"...as a service" which is abbreviated "aaS."   This is based on the 'stack model' of IT, where each layer of functionality depends on the layer below. 

## Broad overview of service models


* Infrastructure as a Service (IaaS):  What your IT department would provide, Nuts and bolts, DIY, Lego.  You need understanding of computing architecture as these services 
* Platform as a Service (PaaS): Everything in between, or pre-configured and managed infrastructure
* Software (aaS): Little to no configuration is needed but these system may be programmable and integrated with other services.  E.g. Office 365, Google Drive

![aaS](https://cloudtweaks.com/wp-content/uploads/2014/07/cloud-stack-images.png)

I believe a sweet-spot for researchers who do not have time to aquire the expertise to manage low-level infrastructure and need something more flexible and programmable than Software, are the platforms.  These are often more expensive than DIY infrastruture, but are faster to provision and provide security controls. 

## Responsibility Model of Cloud Services

| Layer                | Responsibility                  | On-Prem   | IAAS (VM) | PAAS          | SAAS    |
| -------------------- | ------------------------------- | --------- | --------- | ------------- | ------- |
| Network              | Connectivity & Security         | Campus IT | Service   | Service       | Service |
| Hardware             | Maintainance, etc Disk Failures | You/IT    | Service   | Service       | Service |
| Operating System     | Updates, installation, security | You       | You       | Service       | Service |
| Security Software    | Install and maintain            | You       | You       | Service       | Service |
| Server Software      | Install, maintain               | You       | You       | Service       | Service |
| Server Configuration | Tune, Speed,                    | You       | You       | You (limited) | Service |
| User Configuration   | Who can access, user accounts   | You       | You       | You           | Service |
| **Code/Data**        | Doing the actual knowledge work | You       | You       | You           | You     |



What would a "SaaS" offering for your research look like?  A "Google Docs" for your databases?  How about a "PasS" that you could build?   Would it be reproducible by anyone doing the kind of research you do? 

