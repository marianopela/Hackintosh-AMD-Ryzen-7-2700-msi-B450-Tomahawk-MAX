# Hackintosh-AMD-Ryzen-7-2700-msi-B450-Tomahawk-MAX
Hi buddys
This is the repository of my main system based on msi B450 Tomahawk MAX.
You can find the EFI Folder in this repository, the bootloader is OpenCore 0.6.2

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
- [ ] Sleep works only in Mojave and Big Sur, it doesn't in Catalina but it's a common problem
- [ ] Jack mic (common problem with AMD Hackintosh using AppleALC kext)
- [ ] SideCar since the lack of an iGPU
- [ ] etc
