# HP Z230 Hackintosh

### This repo contains ready to use EFI to run macOS Big Sur on HP Z230 Workstation

EFI folder should work on other macOS versions, but it was only tested with Big Sur



Model | HP Z230 SFF Workstation
------------- | ---------------
CPU | Intel Core i3-4150
GPU | Intel HD Graphics 4400
RAM | 8GB DDR3 1333Mhz
Storage | Kingston SSDnow V300 120GB
Software | macOS 11.2.3 Big Sur

## What works?

Everything works fine, but audio is handeled with voodooHDA because AppleALC causes kernel panic

## Instalation

Download this repo. Generate SMBIOS data with [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) and set it in config.plist. Then copy to your EFI partition and that's it.

## What to expect

- Stable and reliable system
- working sleep
- fully working sound including DP 

## How to Install macOS Big Sur

There are two ways you can install Big Sur:

1. If you have an already working macOS, download the Installer from the App Store and make a bootable Installer with `createinstallmedia` by using this command in Terminal: `sudo /Applications/Install\ macOS\ Big\ Sur.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume`

2. If you are using Windows, use [macrecovery.py](https://github.com/acidanthera/OpenCorePkg/tree/master/Utilities/macrecovery) from the offical [OpenCore release package](https://github.com/acidanthera/OpenCorePkg/releases/). Follow this [guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/winblows-install.html) to understand how it works.

After you have created a bootable Installer, copy the EFI folder to the EFI partition and set SMBIOS data generated with [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS). Then install as usual. After the installation, mount the EFI partition of the installed OS and copy the EFI folder to its partition.

## Screenshot

![About this Mac](https://github.com/keczejo/HP-Z230-Hackintosh/raw/main/About%20this%20mac.png)


All this was written on HP Z230 running macOS Big Sur
