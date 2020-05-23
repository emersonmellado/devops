# Introduction to DevOps

![DevOps](/images/whatisdevops/devops-logo.png)

* Why We need DevOps and What is DevOps
* Source Code Management (git & GitHub)
* Setting up our Tool Set
* Python (and why we're learning it in a DevOps course)
* Continuous Integration (jenkins)
* Continuous Delivery (jenkins)
* Virtualization (virtual box)
* Configuration Management (ansible, puppet, chef, terraform)
* Containerization (docker)
* Cloud Computing (AWS, Azure, Google Cloud Platform)
* Continuous Monitoring (Nagios, AWS Cloudwatch, Splunk)
* Final Project
* DevOps for 2020 (new tools / topics in the DevOps pipeline) 

## What do you think DevOps is?
Lets take a few minutes to talk about it. We will use this time to know each other a bit before continuing.

## What is DevOps

Development + Operations = DevOps ~~(simple right?)~~

### What **IS NOT** DevOps

- A technology
- A tool
- A software
- A programming language
- A team 
- _** No wrong definition actually_ :)
 

### Software Development in the 1990's

![Software development in the 1990](/images/whatisdevops/software_delivery_1990.png)

Programmers would write software (mainly in c and c++) and then manually share it with users on servers.
Users would download that software and manually install it on their computers.
People that wrote the software were generally separated from the people that maintained the servers for running the software on.
Bringing software to market was a long, arduous task filled with complicated and error prone steps, resulting in a long development life-cycle.

### Negative points from this process:

- Manually creating software and manually installing software;
- Lots of human errors in the process.
- Separating the process of bringing software to market into two isolated teams tends to create animosity and "its your fault not mine" type of behaviour.
- Software takes a long time to be delivered and another company that is faster and better will drive you out of the market.

From Wikipedia:

> DevOps is a set of practices that combines software development and information-technology operations which aims to shorten the systems development life cycle and provide to shorten the systems development cycle and provide continuous delivery with high software quality.

The introduction of the DevOps practice brought about a merging of the Development Team and the Operations Team into a "hybrid" called "DevOps".

# 1 + 1 = 3

Working together, these teams create a **synergy** that makes working in a software company a pleasure rather than a stressful ordeal.

### New process model
![New Process](/images/whatisdevops/new_process.png)


**Resources:**

[Intro to DevOps](https://www.youtube.com/watch?v=_Gpe1Zn-1fE)

[What does a DevOps engineer do?](https://www.youtube.com/watch?v=o_sUNqZtfVQ)


### Different perspectives on Dev Ops

- from a **Developement** perspective
    - is more focused on creating software, understands code, logical gates, scripting, databases, etc.
    - multiple paradigms, one can be a backend, frontend, full stack
- from an **Operations** *(sysadmin)* perspective
    - is more focused on configuring, keeping up and maintaining servers and computer systems
    - responsible for executing the infrastructure plan
    - monitoring, scaling and sometimes deployment

### Our focus
No assumptions, we will start from scratch. Meaning we will all learn how to to the first steps together. 

> By the end of this course you should be able to create a full scalable infrastructure connected to a CI/CD pipeline.

We will also cover Algorithms, Logic and Python.

*I think we are a bit biased from a dev perspective, probably because this is my main experience.*

You will have to lose the fear of the command line, it is not that scary. :D

### Tools we will use in this course:

1) Virtual Box
2) Ubuntu Linux
3) Python
4) Docker
5) Jenkins
6) Ansible

Peek the desktop stack setup [here](setup.md). We will discuss the setup in more details later on.

[<- Go Back](README.md)
