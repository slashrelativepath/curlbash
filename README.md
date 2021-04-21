# Full Snack Developer
Curriculum for teaching full stack development.


## Getting Started

### Provisioning

1. Download the operating system image. For FullSnax we are using Ubuntu 20.10.

[https://ubuntu.com/download/raspberry-pi]


2. Download and install image copying software.

Raspbery Pi Imager [https://www.raspberrypi.org/software/].

3. Remove SDCard from Raspberry Pi and put into usb adapter and put the adapter into your workstation computer (not the server). If you are not using a Pi put your usb drive in your workstation computer (not the server).

3. Write operating system to sdcard or usb.

* Raspbery Pi Imager
  1. Choose your operating system - Ubuntu Server 20.10.
  2. Choose your sdcard.
  3. Write image.

3. Write wifi config

Remove the sdcard from your computer and re-insert it again to edit the file `system-boot/network-config`. Change "home network" to your wifi name and add your wifi password. 

```
wifis:
  wlan0:
  dhcp4: true
  optional: true
  access-points:
    yournetworkname:
      password: "123456789"
```

4. Remove sdcard from adapter and put back into Raspberry Pi or put usb into server.

5. Turn on server.

6. Open a terminal on your computer.

10. Get IP of server from your computer.

`nmap -sn 192.168.86.0/24` and search for your server named something 'ubuntu'

7. Log in to server from your worksation.
  0. `ssh ubuntu@IPADDRESS` where IPADDRESS is the ip from the previous step
  1. Enter username 'ubuntu' and your password.
  2. If this is the first time logging into the Pi, you will be asked to change your password.
  3. Enter your CURRENT password and then enter in your new password twice.
  4. You will be logged out and will need to ssh in again using new password.

8. Update server to latest software.
  `sudo apt update`
  `sudo apt upgrade`


### Notes

- [https://ubuntu.com/tutorials/how-to-install-ubuntu-on-your-raspberry-pi#4-boot-ubuntu-server]
- [https://ubuntu.com/server/docs/install/autoinstall-quickstart]