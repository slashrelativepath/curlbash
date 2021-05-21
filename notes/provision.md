## Download and install Raspberry Pi Imager

[https://www.raspberrypi.org/software/]

## Download the Raspberry Pi OS 64bit Lite Image

[https://downloads.raspberrypi.org/raspios_lite_arm64/images/raspios_lite_arm64-2021-04-09/2021-03-04-raspios-buster-arm64-lite.zip]

## SDCard

1. Eject or pull the SDCard out of the Pi and put it into the USB SDCard adapter.
2. Put the USB adapter into your workstation.

## Raspberry Pi Imager Settings

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

## SDCard

1. Remove the USB SDCard adapter from your workstation.
2. Take the SDCard out of the adapter and put it back into the Pi.

## Boot
1. Turn on the Pi.

## Find the IP Address of the Pi

1. On your workstation open a terminal or powershell.
2. To get the IP address on Windows type: `Resolve-DnsName USERNAME-pi.local` to get the Pi server IP address.
3. To get the IP address (non-windows) type: `ping USERNAME-pi.local` to get the Pi server IP address.

## SSH to the Pi

1. In your terminal/powershell type `ssh pi@IPADDRESS` to log into the Pi server with the username `pi` and the password `raspberry`.