# Curl Bash Computer Class
Curriculum for teaching computers.

## Provisioning

### Buy a Raspberry Pi 400 and USB SDCard Adapter

[https://www.canakit.com/raspberry-pi-400-desktop-computer-kit.html]

[https://www.canakit.com/mini-micro-sd-usb-reader.html]

### Download and install Raspberry Pi Imager

[https://www.raspberrypi.org/software/]

### Download the Raspberry Pi OS 64bit Lite Image

[https://downloads.raspberrypi.org/raspios_lite_arm64/images/raspios_lite_arm64-2021-04-09/2021-03-04-raspios-buster-arm64-lite.zip]

### SDCard

1. Make sure the Pi is off and or unplugged.
1. Eject or pull the SDCard out of the Pi and put it into the USB SDCard adapter.
2. Put the USB adapter into your workstations USB port.

### Raspberry Pi Imager Settings

1. Run the Raspberry Pi Imager and access the advanced options menu by typing `control+shift+X`.

* Values in all caps like YOURNAME are where you put in your setting.

```
☑ Set hostname: YOURNAME-pi.local

☑ Enable SSH
  Use password authentication
    set password for 'pi' user: raspberry

☑ Configre wifi
  SSID: YOURWIFINAME
  Password: YOURWIFIPASSWORD
  Wifi country: US

☑ Set locale settings
  Times zone: YOURTIMEZONE
  Keyboard layout: US
  ☑ Skip first-run wizard

Persistent settings
  ☑ Play sounds when finished
  ☑ Eject media when finished
  ☑ Enable Telemetry
```
2. Save the Advanced options.
3. Operating System `CHOOSE OS -> Use custom` and pick the `2021-03-04-raspios-buster-arm64-lite.zip` you downloaded.
4. Storage `CHOOSE STORAGE` pick the SDCard you inserted in your usb. Be careful here not to pick your workstation drive.
5. Write

### SDCard

1. Remove the USB SDCard adapter from your workstation.
2. Take the SDCard out of the adapter and put it back into the Pi.

### Boot
1. Turn on the Pi.

### Find the IP Address of the Pi

1. On your workstation open a terminal or powershell.
2. To get the IP address on Windows type: `Resolve-DnsName USERNAME-pi.local` to get the Pi server IP address.
3. To get the IP address (non-windows) type: `ping USERNAME-pi.local` to get the Pi server IP address.

### SSH to the Pi

1. In your terminal/powershell type `ssh pi@IPADDRESS` to log into the Pi server with the username `pi` and the password `raspberry`.

### SSH Keys

1. Create SSH key pair from workstation to server
    1. Type `ssh-keygen` into your workstation terminal
    2. Press Enter to accept the default directory `~/.ssh/id_rsa`
    3. If the default directory already exists you will be asked to Overwrite. Press `y` then Enter

    * Keep in mind this will overwrite your current key pair. Any existing devices that are key paired will no longer authenticate using the previous key.
    4. Press Enter to accept no passphrase
    5. Press Enter again to confirm no passphrase

    * Your public key is now saved at `~/.ssh/id_rsa.pub`

2. Copy your public SSH key to your server
    1. Linux/MacOS: `ssh-copy-id -i ~/.ssh/id_rsa.pub <USERNAME>@<SERVER-IP>`
    2. Windows: `cat ~/.ssh/id_rsa.pub | ssh <USERNAME>@<SERVER-IP> "cat >> ~/.ssh/authorized_keys"`
    * Be sure to replace \<USERNAME\> with your username on your server and \<SERVER-IP\> with the IP of your server

3. Log in to your server to confirm `ssh <USERNAME>@<SERVER-IP>`

### Notes

- [https://ubuntu.com/tutorials/how-to-install-ubuntu-on-your-raspberry-pi#4-boot-ubuntu-server]
- [https://ubuntu.com/server/docs/install/autoinstall-quickstart]