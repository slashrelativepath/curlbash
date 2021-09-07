# Class Notes

### September 8, 2021

What are we trying to get out of this class?

1. Learn to get a computer ready to do work
2. Learn shell (command line) basics
3. Install, configure and run a http service

#### Getting a computer ready to do work

1. physically have a computer
  * review parts of the computer
  * review what happens when you turn on a computer
    - boot sequence
2. put an operating system on the disk
  * put sd card into Workstation
  * install pi imager
  * download OS
  * configure additional settings (cloud-init)
  * image sd card
3. boot the computer
  * put sd card in pi
  * turn on pi
  * wait
4. remote shell (ssh) to the computer
  * find ip address or hostname
  * ssh pi@IPADDRESS

#### Shell basics
  * updating the system
  * shell command format
  * navigation
    - paths
  * files and directories
  * users and permissions
  * installing application packages
  * running applications
  * services
  
#### HTTP service
  * install nginx
  * write config
  * write index.html
  * restart service
  * curl localhost and browser



---

### June 1, 2021

* review PR and merge
* re-image and use SSH keys
* create new user and add ssh key
  * add to script
* set up website deploy
  * from github

  ### first login
  
  ```
  ssh pi@stephen-pi.local

  # in pi
  
  sudo useradd -p $(openssl passwd -1 raspberry) -m stephen
  sudo mkdir /home/stephen/.ssh
  sudo cp ~/.ssh/authorized_keys /home/stephen/.ssh/
  sudo chown -R stephen:stephen /home/stephen/.ssh
  usermod -aG sudo stephen

  exit

  # log in now as your user (stephen)

  sudo apt update
  sudo apt upgrade -y

  sudo apt install -y git

  curl spellcaster.sh/gh | sudo bash

  gh auth login

  # Github.com
  # HTTPS
  # Github credentials - YES
  # Login with web browser - YES

  # copy one-time code
  # go to https://github.com/login/device

  gh repo clone curl-bash/server-config
  cd server-config
  git status

  # update server-config.sh

  # setup github for push

  ssh-keygen -t ed25519 -C "stephen.lauck@gmail.com"
  gh auth refresh -s read:public_key,write:public_key
  gh ssh-key add ~/.ssh/id_ed25519.pub
  git config --global user.email "stephen.lauck@gmail.com" && git config --global user.name "Stephen Lauck"

  # commit / push

  ```

  ### Minecraft Server

  ```
  sudo apt install openjdk-11-jdk-headless 
  curl https://launcher.mojang.com/v1/objects/1b557e7b033b583cd9f66746b7a9ab1ec1673ced/server.jar -o server.jar
  echo "eula=true" > eula.txt
  java -Xmx1024M -Xms1024M -jar server.jar nogui
  ```

  73.185.78.37

  ssh-keygen -t ed25519 -q -C "spellcaster@spellcaster.sh" -f "$HOME/.ssh/id_rsa" -N ""


  ### June 8 2021

  * change adduser -> useradd
  * merge PR
  * re-provision
  * run script

  ```
  git config --global user.name "John Doe"
  git config --global user.email johndoe@example.com
  ```


  ### July 8 2021

  * outside access SSH
  * port forwarding
  * DNS
  * sharing ssh keys (public)
  

  ### July 20

  * finish web site configure
  * build site again
  * copy site from local dir to /var/www
  * fix up script a bit
  * 

  ### July 29 2021

  * processes
  ```
  ps
  ps -aux | head -n 2
  pstree

  ps -ef | head -n 10

  man ps

  ps aux
  ps -ef

  pgrep bash

  # install and start nginx

  pgrep nginx
  pkill nginx

  top

  # install htop

  htop