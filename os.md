# Operating System

### What is an OS?

> An operating system is the primary software that manages all the hardware and other software on a computer. The operating system, also known as an “OS”, interfaces with the computer’s hardware and provides services that applications can use.

![System and Processes](/images/os/system_and_process.png)

### Common OS
- Linux
- Windows
- macOS (Based on UNIX)

### First release
- 1971 - UNIX first release
- 1981 - MS-DOS first release
- 1994 - Linux first release

### Common Devices with OS
- Laptops
- Desktops
- Smartphones
- Raspberry pi
- Datacenters
- etc.

### Processor architecture
- 32 bits - x86
- 64 bits - x64
- arm
- [more about it here](https://stackoverflow.com/questions/29974425/why-is-windows-32-bit-called-windows-x86-and-not-windows-x32)

# Our focus
We will focus on Linux in this course, mainly Ubuntu because it is stable, open source, fairly small and fast.

> If you are really confortable with Linux feel free to use centOS, Fedora or any other distro you'd like just be careful with Arch.

### Linux

[What is linux](https://www.youtube.com/watch?v=zA3vmx0GaO8)

#### Linus Torvalds

In 1991, at the university of Helsinki, Finland,  a 23 year old computer science student purchased his personal computer. It came with an operating system called MS-DOS.

But he wasn't satisfied with it. He preferred using UNIX - the operating system he used at his university. So he went to buy UNIX for his personal use. 
The least expensive UNIX he could buy was $5000. (which is $9412 in today's rate!).
That student was none other than Linus Torvalds.

And that day he decided to create a brand new, from scratch, free UNIX-like operating system - LINUX. And along with help from 100 other developers released  its first version in 1994.

Fast-forward to 2020, LINUX now powers

- All of top 500 fastest super computers in the world
- 96.3% of the top 1 million web servers.
- And 86% of all smartphones in the world (probably includes yours Android, chromeOS...)
- And also, Linux and DevOps tools have a close relationship.
- Tools like Docker and Ansible were developed in Linux first. 


#### Kernel

![Linux kernel](/images/os/linux-kernel.png)

- Permissions

![Permissions](/images/os/Files-permissions-and-ownership-basics-in-Linux.png)
- Folder structure
    ![Directory Hierarchy](/images/os/directory-hierarchy.png)

- Commands
    - Print it an put on your mirror, or your desk this is your new guide! :)
    ![Commands cheat sheet](/images/os/linux-cheat-sheet.png)

### Distros
![Distros](/images/os/linux_distros.png)
- Ubuntu
- CentOS
- Red Hat
- Suse
- Debian
- Fedora
- etc.

### Shell

- What is [the shell?](http://linuxcommand.org/lc3_lts0010.php)

> TL;DR: The shell is a program that takes commands from the keyboard and gives them to the operating system to perform

- [Writting shell scripts](http://linuxcommand.org/lc3_writing_shell_scripts.php)

#### Writting your first shell script

1. Go to your linux VM
2. Create a folder called practicing-scripts
3. Create a file called hello_world: `touch hello_world`
4. Put this content

```bash
#!/bin/bash
# My first script

echo "Hello World!"
```
5. Run the script: `./hello_world`

You should receive an error:

```bash
-bash: ./hello_world: Permission denied
```

This means our script does not have execution permission (the x) part of the permissions. let's set it.

6. Set permissions for the script: `chmod 755 hello_world`
7. Run the script again: `./hello_world`
```bash
Hello World!
```

There you go, you did it!!!

![First shell](/images/os/youdidit.gif)

##### Let's think
- What does the first line means? 
    - The first line of the script is important. This is a special clue, called a shebang, given to the shell indicating what program is used to interpret the script. In this case, it is /bin/bash. Other scripting languages such as *Perl*, *awk*, *tcl*, *Tk*, and **python** also use this mechanism.
- Are extensions mandatory?
- How can I convert my script to a "program like" execution?
- Do I need to care about permissions all the time?
- I've seen echo in PHP, is it the same?

##### Adding script to PATH
Let's first check all global execution places we have:
-  `echo $PATH`

Do you see the current directory in there?
- `pwd`

Let's create a bin folder under my user
- `cd ~ & mkdir bin`

*What is this & sign ???*

This is a sign that allows you to group commands 

# Practice

1. Folder structure, create, delete folders recursively
2. Shell scripts, the more the merrier
3. Study the linux commands from the cheat sheet
4. What does **grep** do?
5. What does **tail** do?
6. How can I create an **alias**?

- Try to version all your scripts using **git**. That way you will learn two things at once.

**Resources**
- Very [cool site](https://linoxide.com/) with lots of linux tips
- Linux commands website: http://linuxcommand.org/
