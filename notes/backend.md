# Backend Engineering

* not customer facing UX/UI
* tools that are accessed by the UI
* tooling for engineers


UI -> API -> Services, Storage, Events


## Full Stack
===
API
===
### Applications / Services
===
### Middleware (applications)
===
### Compute
### Storage
### Network



## Server

virtual machines (operating system)
hypervisor
operating system
hardware

containers
container runtime
operating system
hardware


# Monitoring
# Configuration
# Provisioning

# Roles

* Site Reliability Engineer
* Devops Engineer
* Build & Release Engineer
* Security & Compliance Engineer
* Platform Engineering

Backend Engineering Applications

* deploy applications
* prepare a server for applciation deployment
* build out a topology of servers to support a Services
* update systems and patch applications
* configure system

# Overview 
  ## operating systems
    * unix
    * linux
    * windows
    * mac osx
  ## shell
  ## servers
  ## networking
  ## api requests
  ## database
  ## continuous integration and delivery
  ## storage
  ## secret management
  ## packages
  ## Services
  ## identity
  ## configuration management
  ## source control management
  ## virtual machines
  ## containers
  ## runtimes


1. How is a server provisioned and configured?
  a. what happens when you boot a server?
    1. bios
    2. load os from storage
    3. boot shell
    4. boot desktop
  b. how do virtual machines work?
    1. hypervisors
    2. memory, disk and cpu sharing and isolation
    3. encapsulated operating system on shared hardware
      a. access?
  c. what is a container?
2. shell
  a. navigation
    * cd
    * ls
    * pwd
    * path
      * relative or absolute
    * current / previous directory
    * files and fd and filesystem
    * root
    
  b. files
    touch
    rm
    cat
  c. echo
  &&
  |

3. Users and Permissions


Possible Scenarios:
* install and configure linux on a system
* install and configure an application
* explore SDLC, scm, build, pipeline, storage, deliver, deploy


# Lesson 1
1 hour
## Setup a linux computer
1. get the operating system image
  * download the image for ubuntu server 20.10
2. create a usb drive
  * write the image to the usb or sd
3. boot the usb
4. install the system
5. boot the system

2 hours
## Update a linux computer
1. update all system packages (D)
2. install a new package (D)
  `ssh`
3. write a config
3. run a service

# Lesson 2
 * editing files
 * node web page OR file copy via scp
 * ssh keys
 * create a user
 * enable outside access
 * markdown file
 * create a repo and push up to github (github cli)
 
 # lesson 3
 * create a VM
 * create an API
 * requests (curl)

 # lesson 4
 * auto build and configure
 * have the code to do that


1. make a webpage
2. configure a web server
3. serve a web page




Lesson 1 Notes Realtime
  * commands flags
  * path
  * dot dotdot
  * root /
  * permission
  * RBAC
  * package manager
    * apt
```
# identity navigation and permissions
who
whoami
pwd
ls -la
man ls
ls -la
cd .
cd
# update system
ls /bin
ls /bin | less
# ctrl+c
clear
apt update
# what we did
history
```

CONT...

```
# update and upgrade 
sudo apt update
sudo apt upgrade
ssh

which ssh

sudo -i 

ip a

ssh stephen@192.168.86.47

sudo apt install openssh-server

sudo systemctl status sshd

# check fingerprint


Lesson 5: Networking
  * port forwarding
  * ports
  * security
  * NAT
  * file sharing
    * scp
    * ssh
    * samba
  * ssh keys


Lesson How Computers Work

* parts of the computer
* how boot works


Lesson The Shell
* what is the shell?
* applications vs programs
  what is the difference between
    application and program
    command and application
    command is the whole line for a shell which includes
    applitcaion flags and inputs or args
* order of tokens / command
* execution in shell
  * output
* cat foo
* create and edit file
* redirection
  > 
* rm file

Lesson SSH Keys
* authorized hosts

Lesson Bash Script

Lesson Write a Program

Lesson Virtual Machines

Lesson format
  student always drives
  keep a list of commands or vocab


1. shell is talking to the computer
2. single commands make the computer do stuff
3. make a file with mutliple commands

Lesson ssh/file/copy

* ssh to your server
* cd your home directory
  * cd ~
  * mkdir foo
  * ls 
  * cd foo
  * nano
  * foo.html
  * ls
  * cat foo.html
  * exit
  * download a png on laptop
  * scp cat.png user@serverip
  * add img tag to html
  * need to run a web server
  * install a package, write a config, start the service
  * what is a package - installable package for an application
  * manage with package manager
  * sudo apt update
  * sudo apt install nginx
  * systemctl status nginx
  * man curl
  * sudo apt install curl
  * edit nginx.conf
  * restar the service
  * copy the html and img to nginx web dir
  *  cp ~/index.html .
  * rm index.html
  * mv cat.html index.html
  * tail /var/log/nginx/access.log


  Lesson 86 Game Programming
  * intro to SDL
  * C/C++
  
  Lesson Bash Scripting

  *
  history
  .bash_history
  .profile
  .bashrc
  .ssh

  pipeline
  unix philospholy

  redirection
    stdout


    3/16/21

    review
      * provisioning
        * provide safe access resources
        * enforce risk mitigation
        * going from no computer to backend service running
        * topology
        * scale vertical/horizontal
         