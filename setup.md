# Installing our stack

Make sure you read through and install all the software on the list.

What we will install:
1) [Virtual Box](#install-virtual-box) or [HyperV](#with-hyper-v) or Parallels (Any virtualization software)
2) [Ubuntu Linux](#installing-ubuntu-linux)
3) [Python 3](#python)
4) [Docker](#docker)
5) Jenkins
6) Ansible
7) Git VCS
8) Setup our cloud console on AWS.

- **Resources**
1. [What is a virtual machine (what is virtualization)](https://www.youtube.com/watch?v=yIVXjl4SwVo)
2. [What is virtual box](https://www.youtube.com/watch?v=D1dVhDYAv9E)

---

### Install Virtual box:

1) Navigate [here](https://www.virtualbox.org/wiki/Downloads)
2) Click "Download VirtualBox 6.1"

#### On Windows:
3) Click on Windows hosts
4) [Installation video from community](https://www.youtube.com/watch?v=MTEefDP2Ofo&vl=en)

> (ignore the section on downloading the virtual box binary, as its a little different than using the current version of virtualbox)

#### On Mac:
3) Click on OSX hosts
4) Once downloaded, click on the application in the 
downloads section of you browser
6) Follow the directions on this [video:](https://www.youtube.com/watch?v=lEvM-No4eQo)

#### On Linux:
3) Click on Linux distributions
4) Once downloaded, click on the application in the downloads section of you browser
6) Follow the directions on this [video](https://www.youtube.com/watch?v=_RlsxuayJnI)

---

### Installing Ubuntu Linux

[What is linux](https://www.youtube.com/watch?v=zA3vmx0GaO8)

#### On Windows:

- [To Install Linux 19.04 inside of Virtual Box](https://www.youtube.com/watch?v=pLARQjMwX10)
- [Here](https://www.tutorialspoint.com/virtualization2.0/virtualization2.0_virtualbox.htm) you can find some extra resources on configuring a Virtual Machine on Virtualbox

> ##### With Hyper-V:

There are sometimes issues getting VirtualBox working on a windows host. As a work-around, you can use Hyper-V.

**Note:** Ubuntu 19.04 no longer has updates. We will be using the image without an upgrade. 
- [To Install Linux 19.04 inside of Hyper-V](https://www.bleepingcomputer.com/news/microsoft/ubuntu-1904-now-available-in-the-hyper-v-quick-create-gallery/)
- Ubuntu 19.04 installs in a small box on your screen on Hyper-V. This is a little annoying. The workaround is [here](https://www.donovanbrown.com/post/How-to-run-HyperV-base-Ubuntu-VM-full-screen)


#### On Mac:
- [To Install Linux 19.04 inside of Virtual Box](https://www.youtube.com/watch?v=sNixOS6mHlU)
 
#### On Linux:
- [To Install Linux 19.04 inside of Virtual Box](https://itsfoss.com/install-virtualbox-ubuntu/)
  

---
> **From this point forward you will be performing actions in your virtual machine.**
Now that we all have a working copy of Ubuntu Linux 19.04 installed. We can begin building our **development server**. 

Let's update the apt packages as this will be needed for all installations:
- run: `sudo apt-get update` or `sudo apt update`
---

### Python
 
- [What is a programming language](https://www.youtube.com/watch?v=orCRdBBVLUk)
- [What is python and why it is so popular](https://www.youtube.com/watch?v=Y8Tko2YC5hA)

> We will be using the python 3 interpreter (python3) and the python 3 package manager (pip3). 

1. Install python3:
    *TL;DR*
    - run `sudo apt install python3`
    - run `sudo apt install python3-pip`
    - run `python3 --version` 
    - run `pip3 --version` 
    - If it shows the version you are good to go.
    - If you want more details: [Install Python 3 tutorial](https://tubemint.com/how-to-install-python-3-7-pip-3-ubuntu-19-04/) 

### Docker

- [What is docker](https://www.youtube.com/watch?v=_dfLOzuIg2o)

1. Install Docker:
    *TL;DR* 
    - run `apt install curl`
    - run: `sudo apt install apt-transport-https ca-certificates curl software-properties-common`
    - run: `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`
    - run: `sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic test"`
    - run: `sudo apt install docker-ce`
    - run `docker --version` 
    - If it shows the version you are good to go.
    - If you want more details: [Installation video](https://www.youtube.com/watch?v=lw5eKxMe6dU)

### Git
- [What is Git](https://www.youtube.com/watch?v=uUuTYDg9XoI)

1. Installing Git:
    - run: `sudo apt install git`
    - run: `git --version`
    - If it shows the version you are good to go.
    - If you want more details: [Installing Git tutorial](https://linuxconcept.com/install-git-on-ubuntu-19-04-operating-system/)

> Cloning yout first git repo.

1. run `cd ~`
2. run `git clone https://github.com/emersonmellado/devops.git`
3. run `ls -l`

You should see a **devops** in the folder list.

---

### Jenkins

- [What is Jenkins](https://www.youtube.com/watch?v=LFDrDnKPOTg)

- Installing Jenkins:
    - If you know want to skip a few steps [check this out](https://www.jenkins.io/doc/book/installing/#debian-ubuntu)

    - If you have no idea whete the previous link is all about keep reading:
    - run: `wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -`
    - run: `sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'`
    - run: `sudo apt-get update`
    - run: `sudo apt-get install jenkins`
    - [Installing Jenkins video](https://pkg.jenkins.io/debian/)

- Unlocking Jenkins
    1. Browse to `http://localhost:8080`
    2. Open a terminal and run: `cat /var/lib/jenkins/secrets/initialAdminPassword`
        - If on docker you need to get the [logs](https://www.jenkins.io/doc/book/installing/#accessing-the-jenkins-console-log-through-docker-logs) of the running container, you probably know what to do ;)
    4. Copy the output of that command into the input box
    5. Click continue as an admin

### Ansible

- [What is Ansible](https://www.youtube.com/watch?v=p7-U1_E_j3wK)
- [Installing Ansible](https://www.techrepublic.com/article/how-to-install-ansible-on-ubuntu-server-18-04/)


### AWS Account 

We are going to use the free tier, but feel free to use paid resources, up to you!

1. Browse [here](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc)
2. Click Create Free Account
3. Fill out the form
4. Click continue
5. Fill out that form
6. Click Create Account and Continue
7. Fill out the credit card information:
8. Log in to the aws console with the account id and password we just created.
    email we chose
    password we chose 

 - [AWS Tutorial](https://www.youtube.com/watch?v=XhW17g73fvY)

 [<- Go Back](README.md)
