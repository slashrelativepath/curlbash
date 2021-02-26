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