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

1. Create SSH key pair on your workstation.
    1. Check if you already have an ssh key pair (id_ras and id_rsa.pub) on your workstation. If you do skip to step 3 to copy the key to the server. Note: `~/` is a shortcut path to your home directory.
    `ls -la ~/.ssh`
    
2. Create new ssh key pair. `ssh-keygen -t ed25519 -C "your_email@example.com"`
    1. Press Enter to save the key at the default path.
    2. Press Enter to accept no passphrase.
    3. Press Enter again to confirm no passphrase.

    * Your public key is now saved at `~/.ssh/id_ed25519.pub` and the private key is at `~/.ssh/id_ed25519`

3. Make the .ssh directory on your Raspberry Pi if it doesn't exist
    1. Enter `ssh <USERNAME>@<SERVER-IP> "mkdir -p ~/.ssh"` into your terminal
    * This will make the directory if it doesn't exist, the -p silences the error message if it already exists.
    * Be sure to replace \<USERNAME\> with your username on your server and \<SERVER-IP\> with the IP of your server

4. Copy your public SSH key to your server
    1. Linux/MacOS: `ssh-copy-id -i ~/.ssh/id_ed25519.pub <USERNAME>@<SERVER-IP>`
    2. Windows: `cat ~/.ssh/id_ed25519.pub | ssh <USERNAME>@<SERVER-IP> "cat > ~/.ssh/authorized_keys"`
    * Be sure to replace \<USERNAME\> with your username on your server and \<SERVER-IP\> with the IP of your server

5. Log in to your server to confirm that the ssh keys are working `ssh <USERNAME>@<SERVER-IP>`. You should no longer be asked for a password to connect to the pi server.

### Notes

- [https://ubuntu.com/tutorials/how-to-install-ubuntu-on-your-raspberry-pi#4-boot-ubuntu-server]
- [https://ubuntu.com/server/docs/install/autoinstall-quickstart]
