# Nature of Cloud Computing
## ARCHIVE: see current website <br />https://icer.msu.edu/cloud-computing

## Some Motivation at Amazon.com
- Massive IT infrastructure supports  the Amazon store and company <!-- developers, accounting, sales, testing, administration, etc -->
- They wanted to sell shopping application as a service to a company like Target who didn't want to r-un their own store. T This required the software developers to have lots of flexible infrastructure (servers) to run on.  
- They found team to build a service (with software) could spend 70% of their time setting up the 'back end' 
 - They called all the infrastructure needed to run a massive dot-com "muck" and saw this as a secondary supporting role to application development.    What they wanted in days actually took months.  

### Eureka moment for Amazon: we could sell it
   
- Amazon automated their IT department so teams could order and provision the servers they needed on demand beyond just virtualization ("everything was an API")
- They got really good at running very large data centers for many customers as cheaply as possible and on-demand for Amazon.com and  other stores and services.   
- They realized that their innovations would help any IT organization and especially internet start-ups like themselves, and that they could sell it.  
- Their customers were other IT departments  
*Blog Post from 2006: ["We Build Muck, So You Don’t Have To"](https://aws.amazon.com/blogs/aws/we_build_muck_s/)*

<!-- ### Case studey: D2L course management system
 
MSU originally ran, or 'hosted' started by aquiring the web application software and associated systems, building all of the hardware (servers), disk space to hold it all, newtork to connect them, data center space and when you connected to D2L, you connected to a system on the MSU campus. 

- Scalability : when demand was very high, the system was overwhelmed
- Maintainablility: required many people to keep it running
- Cost: The company "bright space" offered to host D2L for institutions.  The student experience is identical.  MSU switch to that model and saved money.  D2L was slow this week becuase now when we access D2L we share infrastructure with everyone in the world.   -->


## NIST defintion of cloud

Government offices interested in purchasing cloud computing needed a definition of it to differentiate from other kinds of computing, hence... the [NIST definition of cloud computing](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-145.pdf) essential characteristics 

- **On-demand self-service**. 
- **Measured service**: pay for what you get.   
- **Broad network access**: accessible from the internet
- **Rapid elasticity**: no limits from a customer perspective.  This word was invented by AWS
- **Resource pooling**: single resources serve many customers.  

<!-- ## Other Web-based services that are _not_ cloud computing

 - **Web hosting** Focused on providing offered many of these features but was limited in service offerings.   I've used a company called dreamhost since early 2000 to provide websites for non-profits and commercial customers, but also email and storage and limited database services.  

- **Co-location** Bring your own hardware, eg. Data Center only

- **Server Rental** Servers on the internet you could use for various things, primarily web sites & applications.   (Rackspace) 

- **Other remote computing services** example sending your accounting data to an external service for processing (which now seems quaint).  EDS from the 80s 90s by Ross Perot provided IT and Data services to major corporations primarily GM.  -->

## What is Cloud Computing? Cloud concepts vs Cloud Providers
  
- Three major cloud providers are in a constant arms race, literally (*[Azure vs. Amazon competed for a $10B defense contract](https://www.theregister.com/2022/04/28/nsa_wands_aws/)*):  Azure, Amazon Web Services and Google Cloud Platform

- Offerings are very similar so all are great choices
- other options, smaller companies, open source options (used by Indiana University [JetSteam](https://jetstream-cloud.org/) HPC,  [Osiris project](https://www.osris.org/) from MSU, UMich, Wayne State and IU.   [Cyverse](https://cyverse.org) for running jobs.


##  Benefits of Cloud Computing for Research 

  - Customized Computing: can create customized resources only when you need it
  - Elastic/On-demand: can run ad-hoc computations on those on-demand resources
  - Instant service: 
  - Reproducible: a computation can be re-run as needed, meaning cloud resources can be easily re-recreated to re-run your computations. 
  - Cost effective: unlike commerical applications, more users does not mean more revenue.   Budgets are fixed and the pay-as-you-go model requires vigilance to not over-spend.   
  - Others? <!-- discussion -->

**Restatement of goals of this Cloud Computing Fellowship:** 

- Learn which types of computing resources are beneficial to your research
- Learn how to use Cloud to create those resources
- Use the services packaged by cloud companies to discover new resources


## Using workflow and computational thinking 

- Karl Popper stated that "non-reproducible single occurrences are of no significance to science" ( *K Popper, "The Logic of Scientific Discovery", English translation from Routledge, London, 1992, p. 66.*) and this is a significant issue for research based on computing.

To enhance reproducibility in your own work, consider documenting all the steps needed for create the environment to run your computation.   For many on-premise academic systems (e.g. the MSU HPCC), we depend upon the system administrators to create that environment, but we may install and configure all the software we need to run our code.   Workflow thinking can apply to the scienfic domain itself (e.g. "Principles for data analysis workflows" https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008770 )  and to the provisioning of the cloud computing environment.   That is, we may use a workflow system for creating all the cloud stuff we need, and then a different workflow system that runs on that cloud stuff.   One example is we may [create an HPC system on Azure using templates](https://azure.microsoft.com/en-us/resources/templates/create-hpc-cluster/) and then launch the Slurm scheduler on that HPC to run our jobs.  (*note the complexity of running your own HPC is beyond the scope of this fellowship and used as an example only*)

A major advantage to using workflows or code for provisioning your cloud computing components is that you can turn them off and delete them when you are done, and restart when needed.   

Our first uses of cloud will use forms to create resources, but we encourage you to automation where possible.  


## About Cloud Security

Security and Risk management are important issues even for researchers who's data are open   
- If your computer is a **server**, your responsibility just increased 100X: these are prime targets.    Consider each component of a server to be a point of vulnerability.   
- Finding a readable list of security recommendations for cloud computing is a challenge for all the reasons outlined above.  Our textbook has [a nice chaper outlining cloud security](https://s3.us-east-2.amazonaws.com/a-book/security.html)
- We will cover methods to reduce security risks but it's important to consider the risk of hacking from the beginning

Attackers  may use the services you create to launch attacks on other services, leaving you liable.  

- The "Shared responsibility" model for cloud computing takes a model of computing components, and shows how much of each component the user is responsible for security.  
 
![Microsoft Model of Shared Responsibility](../img/microsoft-shared-responsibility.svg)
*[Microsoft Model of Shared Responsibility for Cloud Computing](https://docs.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility)* 

We will come back to this model as we gain deeper understanding of research computing on the cloud. 

## HPCC vs Cloud

- [Dr. Parvizi's white paper](../references/DRAFT_cloud_computing_for_academic_research_parvizi_2021.pdf) outlines the challenges of adapting HPC workflows to cloud computing.  

The HPC is amazing effective at running all kinds of systems at very list cost, if any, to MSU researchers, but not all are the best fit.  

Many systems not designed for HPC can be adjusted to run in that environment.  However, just like many workflows are difficult to port from HPC to cloud, some cloud workflows are difficult run on HPC (but never say never).  Especially windows-based software. 

<!--
- Big Data systems
- Long-running Data Systems like database servers
- Web-based applications
- Windows
- Systems with complex or specific configuration needs -->


## Acknowledging bias in access to cloud computing across research cultures

It's widely recognized that AI is frequently bias.   For example, Azure Voice recognition did not work for a female researcher who developed voice-controlled surgery, so 

However I believe there is also inherent bias in the user interfaces, design and definitions in the engineering of technology across many axes of diversity (gender, culture, background, training, creativity, etc).  System Engineering is it's own discipline and Cloud computing is arcane so our goal is to reduce conceptual barriers to using this technology while you work with us. 
 

## About Cloud Costs
- Cost management is a major hurdle for adopting CC, so we will talk about costs extensively
- (Almost) everything you do in Azure has a cost
- Costs often acrue over time, wether the resource is in use or not
- Deleting resources when are not using is a great way to reduce cost
- We want to encourage you to experiment!  Using a very powerful machine for an hour may cost only $0.50  
- Just be aware that creating something and leaving it on will deplete your budget
- Solution: "Budget Alerts"

Case Study: Computation of a machine learning model based on gene networks for inferring gene association ( https://www.geneplexus.net): a single (virtual) machine to run the ML such that users would not have to wait too long would be $650/month.  However, if the computational power is provisioned only when needed, it's 5 cents/job.    


## Value Proposition of Cloud Computing 
- Costs are more than just dollars for services.  Consider `[Total Cost] = ( $ + Time + Risk )`
- `[Total Time] = ( development time + wait time + compute time ) `
-  Security Risks are rarely non-significant, so factor that into cost
- In the Service level spectrum, the higher level "platform" services may have higher monetary costs but often reduce time and risk


<!-- 
Summary and additional comments

summary: freely explore cloud services using the portal as there are often free-tiers; try the programming interfaces  at least once as this will make your work reproducible ; security is always a concern and consideration of cost ; look to the higher level services, even though more expensive may be faster to results and more secure 


Types of services ( do not say "as a service or AAS)
software, platform, infrastructure

describe each, 3 is not part of CCF. some
do not fit easily in this framework ( GEE ). on 2nd 2

Pre-cloud history : important because services now use these words and metaphors to map on to services. the people who used tech historically were customers of the cloud so the cloud had to make sense to the IT people it was sold to.

Client/Server: email, shared files, unix she'll, ftp. server = software that listens and acts
web - more passive than any of the others.
web search server system.
server can be in office or on web. if on the web it's a computer that hosts server
a website needs 1) web content 2) web server software 3 ) computer on the internet to run that software. 1 is easy.

web site vs web application distinction.

web 2.0so popular , web platform companies showed up in 90s : dreamhost, rack space
service was limited to stuff to run a web app = content + code, server, db, storage
( describe the customer , who uses this service ). example Bee Database
advantages vs running your own web server
big web company needed to still run their own stuff.

different topic

enterprise computing : bought rooms full of expensive hardware, networks and software: company data systems, file storage , company run email, moving huge data , etc. "main frame"

HPC : bought rooms full of really expensive hardware and really expensive networks. software was free.

computer == box. each box needs management hardware & software.

box for not flexible. solution : virtualization
one huge box, many virtual computers. can create

"provisioning" is hard work. hardware,operating systems, software etc.

how annoyed are you when you have to run an update? imaging you had hundreds or thousands of boxes to keep updated, that hundreds/thousands of people depend on. then hard drives crash. chips fail etc

every work group has special needs.

what does this mean for researchers? we have an HPC to run stuff. why do we also need cloud.
- window apps
- special configuration: eg getting the Unity game engine to run on our HPC ( for evolution simulations ) meant hacking the binary header of the program to trick it. many others are not so lucky that a solution is ever found.

data systems
web based programs.
the HPC is amazing but it is not great for everyone or everything.
Researchers had to DIY ( my friend Jason ) , find a computer person( like I was in the past ) or beg the IT department to get them what they need.

other things were put in place for enterprise or google ( containers, custom hardware etc ) but


-->
