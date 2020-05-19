

ANSIBLE

What is ansible



Ansible is an open-source software provisioning, configuration management, and application-deployment tool.

It is used for IT tasks such as configuration management, application deployment, intraservice orchestration, and provisioning. 

Automation is crucial these days, with IT environments that are too complex and often need to scale too quickly for system administrators and developers to keep up if they had to do everything manually.




WHY ansible



Free to use by everyone.
It does not need any special system administrator skills to install and use Ansible.
Great modularity (plugins, modules, inventories, and playbooks) Lightweight and consistent, and no constraints regarding the operating system or underlying hardware.
Very secure due to its agentless capabilities and use of OpenSSH security features.
Smooth learning curve determined by the comprehensive documentation


How it works



Ansible uses playbook to describe automation jobs, and playbook uses very simple language (i.e. YAML) which is easy for us to understand, read and write. 

Ansible is designed for multi-tier deployment. It does not manage one system at time, but it models IT infrastructure by describing how all of your systems are interrelated. 

We connect our nodes through ssh and after that, Ansible pushes small programs called as "Ansible Modules". It runs those modules on your nodes and removes them when finished. Ansible uses the hosts file where we can group the hosts and can control the actions on a specific group in the playbooks.

How it works




Installing ansible



There are two types of machines:
Control machine Machine from where we can manage other machines.
Remote machine Machines which are handled/controlled by control machine.

There can be multiple remote machines which are handled by one control machine. So, we have to install Ansible on control machine.
Ansible can be run from any machine with Python 2 (versions 2.6 or 2.7) or Python 3 (versions 3.5 and higher) installed.
 Note: Windows does not support control machine.

By default, Ansible uses ssh to manage remote machine

Installing ansible



We are going to install Ansible on our Ubuntu machine (local or virtualized one)

$ sudo apt-get update 
$ sudo apt-get install software-properties-common 
$ sudo apt-add-repository ppa:ansible/ansible $ sudo apt-get update 
$ sudo apt-get install ansible

And that's it! Now you are ready to manage remote machines!


Understanding YAML



YAML uses simple key-value pair to represent the data. The dictionary is represented in key: value pair.
This is an example of part of a Playbook:

- hosts: group1
 tasks:
 - name: Install lldpad package
 yum:
 name: lldpad
 state: latest
 - name: check lldpad service status
 service:
 name: lldpad
 state: started

Note: we recommend you to read more about YAML format!

Ad-hoc commands



These are commands which can be run individually to perform quick functions. 
For example, if we have to reboot all our company servers, we'll run the Adhoc commands from '/usr/bin/ansible'.
These commands are of one time usage.

1) Reboot all our company servers in a group, 'abc', in 12 parallel forks 

$ Ansible abc -a "/sbin/reboot" -f 12

2) Transferring file to many servers/machines

$ Ansible abc -m copy -a "src = /etc/yum.conf dest = /tmp/yum.conf"


Ad-hoc commands



3) Create new directory

$ Ansible abc -m file -a "dest = /path/user1/new mode = 777 owner = user1 group

4) Deleting directory and files

$ Ansible abc -m file -a "dest = /path/user1/new state = absent"

Ad-hoc commands



Ad-hoc commands are available for YUM and APT as well:

1) Check if a yum package is installed or not, no update.

$ Ansible abc -m yum -a "name = demo-tomcat-1 state = present"

2) Check is the package is not installed.

$ Ansible abc -m yum -a "name = demo-tomcat-1 state = absent" 

3) Check the latest version of package is installed.

$ Ansible abc -m yum -a "name = demo-tomcat-1 state = latest"

Ansible playbook



Playbooks are the files where Ansible code is written and are used in complex scenarios. 
Playbooks use YAML format, so there is not much syntax needed, but indentation must be respected. 
Ansible playbooks tend to be more of a configuration language than a programming language.

Like the name is saying, a playbook is a collection of plays. Through a playbook, you can designate specific roles to some of the hosts and other roles to other hosts. By doing so, you can orchestrate multiple servers in very diverse scenarios, all in one playbook.

Playbooks contain the steps which the user wants to execute on a particular machine. Playbooks are run sequentially.

Ansible playbook



YAML is a strict typed language so we need to write with extra care. We'll use a simple editor like notepad++. Open it and write the below yaml and change the language to YAML (Language YAML). Name the file test.yml

--- 
 name: install and configure DB
 hosts: testServer
 become: yes

 vars: 
 oracle_db_port_value : 1521
 
 tasks:
 -name: Install the Oracle DB
 yum: <code to install the DB>
 
 -name: Ensure the installed service is enabled and running
 service:
 name: <your service name>

YAML TAGS



name
Specifies the name of the playbook describing what this will be doing. 

hosts
Specifies the lists of hosts or host group against which we want to run the task. The hosts field/tag is mandatory. The tasks can be run on the same machine or on a remote machine. 

vars
Lets us define variables to be used in our playbook. Usage is similar to variables in any programming language.

tasks
Contain tasks to be executed. Tasks are a list of actions needed to be performed. A tasks field contains the name of the task. Each task internally links to a piece of code called a module. A module that should be executed, and arguments that are required for the module you want to execute.

Ansible roles



Roles provide a framework for fully independent, or interdependent collections of variables, tasks, files, templates, and modules.

The role is the primary mechanism for breaking a playbook into multiple files. This simplifies writing complex playbooks, and it makes them easier to reuse. 

Each role is limited to a particular functionality or desired output.

Ansible roles



Roles provide a framework for fully independent, or interdependent collections of variables, tasks, files, templates, and modules.

The role is the primary mechanism for breaking a playbook into multiple files. This simplifies writing complex playbooks, and it makes them easier to reuse. Each role is limited to a particular functionality or desired output.

Roles have a structured layout on the file system. The default structure can be changed.

Each role is a directory tree in itself. The role name is the directory name within the /roles directory. We'll use the instruction ansible-galaxy

Ansible roles



ansible-galaxy init role1

If we write tree role1 we'll see the directory structure of role1

Now we'll create a playbook for demo purpose. The playbook is called role1_orchestrate.yml. We have defined the hosts: tomcat-node and called the two roles – install-tomcat and start-tomcat. What we want to do is that we have a war which we need to deploy on a machine via Ansible.

--- 
- hosts: tomcat-node 
roles: 
 - {role: install-tomcat} 
 - {role: start-tomcat}

Ansible roles



Once we create the roles, there will be a "roles" folder, with directories for each of the created roles.
Inside those directories, you'll find a "tasks" folder, with a main.yml file on it.

The advantage of breaking the playbook into roles is that anyone who wants to use the Install tomcat feature can call the Install Tomcat role.

Some practice



We'll play a little bit. Work as groups of 3 people. Install one control machine and two remote machines.

Create a playbook that will install and start tomcat
Run Ad-Hoc commands to copy files into the hosts
Create a new Directory. Copy a file into the Directory
Reboot your hosts

Some homework



Do your research at home about how to use the following on Playbooks:

Variables
Exception Handling
Loops
Conditionals

