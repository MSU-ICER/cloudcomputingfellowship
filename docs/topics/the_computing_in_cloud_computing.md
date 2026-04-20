---
title: The Computing in Cloud Computing
---
# Helping to Understand the "computing" in cloud computing
## ARCHIVE: see current website <br />https://icer.msu.edu/cloud-computing

![](../img/header_image_old_corp_network_diagram.jpg)

You come to us with a unique set of experiences with computing, with more or less experience depending on your previous needs.  A challenge we have seen, for the many years we've been helping people, is understanding the context of computing in their research to understand the tools they have available.    

In fact most documentation for cloud computing assumes you know the world of computing.   [An introduction to cloud computing from microsoft](https://learn.microsoft.com/en-us/training/modules/describe-cloud-compute/) lists this  Prerequisite: "Basic familiarity with IT terms and concepts."  It turns out 'basic' can mean a lot of things.

**A core goal of the MSU Cloud Computing Fellowship is to help you connect cloud computing to your research in a meaningful way**

our original question: 
- How can *cloud computing* benefit help your research?

Let's re-frame the question for this discussion:
- Which kind of *computing* could help my research?
- Can I use that kind of *computing* in *the cloud*? \
  That is, could cloud computing enable me to use computing I otherwise couldn't?

You may already have an idea of what this is, and experience with computing but many who come to us know it's valuable but are ready to learn why.  

## What is computing? Minimal Vocabulary
 
Cloud computing was invented for, and is marketed to IT systems administrators, software developers, and IT/technology managers.  See the history of AWS.   It is was not designed with researchers in mind.   Most training and documentation  Note, however, that Cloud Computing is general enough and is often marketed to researchers or 'for research.'  

The primary function of cloud computing is to provide "infrastructure" aka the "back-end" or back room of a company's IT department, so we ware going to learn about that.  In fact, cloud computing is frequently defined, named, and sold based on abstractions of physical components of computers and IT infrastructure.    Hence learning more about IT infrastructure, or "computing" may be helpful understanding the context in which cloud computing is engineered.  This can help you determin what you may need from cloud computing to get your research done.   

Could you purchase your own infrastructure (computers, networks, disks, etc) and run it "on-premise" and get the same benefit as cloud computing?  Or have your institution do that?  Sometimes yes!  The MSU HPCC is a great example when on-premise is more beneficial and cost-effective than cloud computing.   

## About Computing: Major components of computer

Of course you know what is in a computer. The goal is to come to common understanding, and to frame for extension to cloud, and to find the cloud services that mimic these features.  

- User software (scripts, user code, etc)
- Base Software (programs to run scripts such as Python, Rstudio, Stata, Fluent, etc etc and/or libraries to compile code such as the gcc compiler, etc)
- Operating System (needed to make the computer functional)
- Input/Ouput (I/O, infrastructure to get data in and out of a computer, primarily network connections but also USB) 
- Storage - external ( attached or via network or other I/O )
- Storage - local disk
- Central Processor (CPU) & Memory (RAM)
- Computer Architecture (model type)
- Network

Where is the data in this abstraction of computer infrastructure? Answer: everywhere

If you hadn't thought or known about the components of a computer, that's no mistake.   Most people don't know the details of how their car operates, how to change their oil, or diff between carburetor and turbo charging?

### "Stack Model" of computing.  

Just as in Science and the humanities, we need a model and terminology to talk about a subject.  A standard IT model of a computer is a 'stack' model, where each upper layer depends upon the layers below.   Most models of cloud computers build upon this simple model.  

<table border="0">
<tr><td align="center">User</td></tr>
<tr><td align="center">Interface/Connection</td></tr>
<tr><td align="center">Software</td></tr>
<tr><td align="center">Operating System</td></tr>
<tr><td align="center">Computer Hardware: CPU & RAM</td></tr>
<tr><td align="center">Data Storage</td></tr>
<tr><td align="center">Network</td></tr>
</table>

## About Computing: What is a server?

Cloud computing started with, and frequently talks about  "*servers*," so we should define that. 

A server is any computer running software that listens for, and responsed to, messages.  For a server to be useful it should be connected to a network but it doesnt' need to be.  Some terms:
 - The 'server' is actually the software, not the hardware.  You can run a server on your laptop. 
 - The computer that runs the software is the 'host'
 - A 'client' is software sends the message, and receives and interprets the response.   
 - the protocol is the method by which you exchange messages.   Now it is almost exclusively web (http) but there are many others
 - the form the input message can take, and the form of the message that is returned is known as the API of the server.  it's the interface that you have to work with. 
 - port: a computer may run many servers for internal and external use.  Unix devised a system of numbered 'ports' (nbumber 01 to 64K), and when running a server you must tell the server which port to listen for messages.  Users of most software never have to know or think about ports.  

The 'Client/server' model invented in the 60s is so successful that we use servers for our daily lives and don't think about it (except when the server is down).  This model of computing is important because it's at the basis for of cloud computing.  

We often think of a server as a box, but in the model above, the server is in the software layer, but each of layers below provides services for that software to exchange messages with another computer.   If you can abstract, virtualize or automate the layers below, it becomes much easier to provision servers than to purchase, install and configure physical hardware.   


### Example Server

A Web server is a well known, easy to use, and very useful server to run.  The terms above translate as follows:

 * server is any machinge (including your laptop) running a program that listens for http messages on port 80. client is a web browser
 * message:URL which includes address, url paths, and additional parameters <!-- this is only part of the message but is a necessary part -->
 * response: several headers including the status of the request (that we rarely see) and ultimatley the contents of the web page
 * client interprets the code and renders the page.   
 * an alternate client could be a script, or the `curl` utility
 * `https://www.amazon.com/dp/B09VXBNTJ1/ref=sr_1_93?brr=1`

What is the host in this URL?  What is the message?  We could spend a week talking about web servers, protocols and a year about programming web server.  The important thing is that  there is a host computer, the 'web server' software on the host listening for requests, and the client(s) connecting to it to retrieve files. 

### Other Types of Servers

- **Database** Client: special database client (not web browser) sends data commands as messages, response is tabular outputs
- **File Servers**  Share files.  We use Cloud file sync services, but 
- **Collaboration** Email, calendaring etc
- **Enterprise Data Systems** for loading, cataloging, transforming business data
- **Security** Firewalls, Proxy, network traffic management
- **Monitoring** system health data collection, accessible via another web server
- **Web-based services** For example D2L.  

Many of these do not use web-based protocols or connections.   They define their own protocols, either as a public standard (e.g. email) or proprietary standard (database)


### Servers and Networks

**Networking Requirements to access a server:**

- the server must be on the same network as you to receive your message 
  *I can run a web server right on my laptop, but you couldn't reach it.  the network is me talking to myself*
- the more accessible the network, the more vulnerable, so partitioning is used
- servers that accept messages from the Internet are a major security risk
- network failure stops all work for everyone
- designing efficient, robust, and secure networks is a major resource drain

Why do I think this is important?  not only can you make a server (web, data, cluster, etc with cloud but everything you interact with in cloud is a server.  You will see many services dedicated to networking in the cloud.  

On our campus, the network is managed by the institution, and it is configured to block all incomming traffic to prevent anyone from running a server which is a security risk. 

## Too much hardware? Virtualization to the rescue

If you run a big IT Department that services 1000s of people, you need a lot of servers.   Each server can only handle a certain amount of 'traffic.'  Hence there are many methods for connecting multiple servers to act as one big server.  Each physical machine requires 1) installation 10) maintainence.  

- IT Departments 'serve' large user communities with large amounts of infrastructure.  Techniques were invented to separate the 'server' or 'network' from the hardware.   
- Virtualization: single box with a layer of software to share among different software. 
- Many servers could be created and managed with software on a single hardware  
- Virtualization was a necessary conceptual and technological innovation to pave the way for cloud computing and is widely used both on-premise and in the cloud.
- Networks and other services followed suit: create single big computers that uses 'virtualization' software to emulate the functioning of a service, such that the clients don't know  they are not working with an abstraction.    Running different wires to connect different things is labor intensive.   



