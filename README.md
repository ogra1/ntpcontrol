# ntpcontrol snap

This snap allows setting an ntp server on an Ubuntu Core system via confined snap commands.

## Interfaces
You need to connect the ntpcontrol:timeserver-control with the following command to allow it access to the timeserver config:
```
snap connect ntpcontrol:timeserver-control
```

## Commandline tool
It ships a commandline tool you can run like:
```
sudo ntpcontrol set ntpserver=ntp.ubuntu.com
```
and you can unset the ntp server again with:
```
sudo ntpcontrol off
```
**Note that you need to reboot your system for the change to take effect !!**

## Usage in images
If you are adding this snap to your default image via the required-snaps option in your model assertion
you can define a default in your gadget.yaml like:

```
defaults:
  TIl6Xtz7Xva7BKcIetWFL9UTz9L0fS3G
    ntpserver: ntp.ubuntu.com
```
