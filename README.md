# Hackintosh-AMD-Ryzen-7-2700-msi-B450-Tomahawk-MAX
Hi buddys
This is the repository of my main system based on msi B450 Tomahawk MAX.
You can find the EFI Folder in this repository, the bootloader is OpenCore 0.6.1
![About This Mac](https://github.com/fill0r4/Hackintosh-AMD-Ryzen-7-2700-msi-B450-Tomahawk-MAX/blob/master/Docs/About%20This%20Mac.png?raw=true)
![Setup](https://github.com/fill0r4/Hackintosh-AMD-Ryzen-7-2700-msi-B450-Tomahawk-MAX/blob/master/Docs/Setup.jpg?raw=true)

## Hardware
- CPU: AMD Ryzen 7 2700
- MOTHERBOARD: msi B450 Tomahawk MAX
	- Audio: Realtek ALC892 
	- 1Gbit Ethernet: Realtek 811H
  - 1x USB-C USB 3.2 Gen 2
- RAM: 16gb Crucial Ballistix Sport 3000mhz CL15 (overclocked to 3200mhz CL14)
- STORAGE: 
   - SSD nvme Silicon Power A80 1tb (Windows)
   - SSD Crucial MX300 275gb (macOS)
- GPU: Sapphire Radeon RX 580 8gb Nitro+ SP
- COOLER: Deepcool Castle 360ex white
- FANS: 3xLL120 Corsair
- CASE: Corsair iCue 465x white
- PSU: Corsair TX650M
![Build](https://github.com/fill0r4/Hackintosh-AMD-Ryzen-7-2700-msi-B450-Tomahawk-MAX/blob/master/Docs/Build.jpg?raw=true)


## What's Working?
- [x] Tested with macOS Mojave 10.14.6, Catalina from 10.15.4 to 10.15.7 and Big Sur Beta 6
- [x] QE/CI Graphics Of Sapphire Radeon RX 580
- [x] Restart and Shutdown. 
- [x] Rear Jack (Green) + Front Speaker Jack (Headphone)
- [x] HDMI Audio
- [x] HDMI Output
- [x] Display Port Audio
- [x] Display Port output
- [x] HEVC and H264 Encode for RX 580
- [x] All USB ports at full speed (including USB-C)
- [x] etc

## What's not Working?
- [ ] Sleep works only in Mojave and Big Sur, it doesn't in Catalina but it's a common problem with AMD CPUs
- [ ] Jack mic (common problem with AMD Hackintosh using AppleALC kext)
- [ ] SideCar due to the lack of an iGPU
- [ ] etc

## Benchmark
-GeekBench Scores: [CPU](https://browser.geekbench.com/v5/cpu/3910230) [GPU](https://browser.geekbench.com/v5/compute/1548862)
![Cinebench Scores](https://github.com/fill0r4/Hackintosh-AMD-Ryzen-7-2700-msi-B450-Tomahawk-MAX/blob/master/Docs/Cinebench%20Scores.png?raw=true)

## Installation steps
1. [Create a macOS USB-Installer stick](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
2. Copy the EFI folder you downloaded from this repository into the USB stcik EFI partition if you created it in macOS or into the Root of the USB Stick if you created it in Windows. 
3. Download [Propertree](https://github.com/corpnewt/ProperTree) and use it to edit the EFI/OC/config.plist file; add your mac address into the PlatformInfo/ROM section
4. Download and open [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS), pick the option 1 to download and update macserial then use the option 2 to select the EFI/OC/config.plist file and the option 3 to generate a SMBIOS, type iMacPro1,1 and enter.
5. Adjust your BIOS settings according to the [Dortania Guide](https://dortania.github.io/OpenCore-Install-Guide/AMD/zen.html#amd-bios-settings) 
6. Boot the USB-Stick and install macOS

## Post install steps
1. [Copy the EFI folder into the EFI partition of your macOS drive](https://dortania.github.io/OpenCore-Post-Install/universal/oc2hdd.html#grabbing-opencore-off-the-usb) in order to boot without the USB-stick
2. I suggest you to [create a USB Map](https://dortania.github.io/OpenCore-Post-Install/usb/) for your system and delete mine (USB-Map.kext) because it will likely cause you issue.
3.For every issue you can refer to the [Dortania guide](https://dortania.github.io/OpenCore-Post-Install/)
4. If you want you can [change the CPU Name](https://forum.amd-osx.com/index.php?threads/change-cpu-name-on-catalina.298/#post-1222) in About This Mac

## Credits
- [Dortania](https://github.com/dortania) for the Opencore Desktop Guide
- [Acidanthera](https://github.com/acidanthera) for too many things to mention each, starting from Opencore bootloader to a lot of crucial kexts...
- [CorpNewt](https://github.com/corpnewt) for ProperTree and GenSMBIOS scripts
- [Trulyspinach](https://github.com/trulyspinach) for SMCAMDProcessor.kext, AMDRyzenCPUPowerManagement.kext and AMD Power Gadget app.
- [chris1111](https://github.com/chris1111) for the Opencore theme which I used in this EFI folder

Regards, Filippo aka fill0r4
