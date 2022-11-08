# Hackintosh-OptiPlex-7070-SFF

Forked from [cyg02032015/OptiPlex-7070-SFF](https://github.com/cyg02032015/OptiPlex-7070-SFF)

<img width="392" alt="截屏2022-11-08 16 47 05" src="https://user-images.githubusercontent.com/68957257/200517946-248c2454-615a-4118-a3b9-1c21c7f030d6.png">

**Opencore Bootloader 0.8.5. Tested on Ventura 13.0**

## Hardware Specs
* **CPU: Intel® Core™ i7-9700**
* **iGPU: Intel® UHD Graphics 630**
* **GPU: Radeon™ RX 560 (low profile)**
* **RAM: 32GB DDR4 2666 Daul Channel**
* **HDD: TOSHIBA RC500 NVMe SSD 500G**
* **LAN: Intel I219LM7**
* **Wi-Fi & Bluetooth: BCM943602CS with PCI-E&Onboard-USB (HS04 on the motherboard) **

## Working
* CPU Turbo Boost & Thermal Throttling
* Radeon™ RX 560 & iGPU acceleration
* ALC 255 audio
* All USB Ports
* LAN & Wireless Network
* Airdrop & Airplay
* Sleep & Wakeup

## Not working
* 

## BIOS Settings
* General → Advanced Boot Options: ***uncheck***
* System Configuration → SATA Operation: ***AHCI***
* Secure Boot → Secure Boot Enable: ***Disabled***
* Intel® Software Guard Extensions™ → Intel® SGX™ Enable: ***Disabled***
* ~~Power Management → Block Sleep: ***check***~~
* Virtualization Support → VT for Direct I/O: ***uncheck***

## BIOS Settings via GRUB (Optional)
* Set Pre-Allocated DVMT to 64M: 
***setup_var 0x8DC 0x02***
* Disable CFG lock: 
***setup_var 0x5BE 0x00***

## USB Mapping ##

![usbports](https://user-images.githubusercontent.com/68957257/200523324-7c6c3393-8f48-4d1a-a051-366b00ef05d4.png)
<img width="1175" alt="截屏2022-11-08 17 15 35" src="https://user-images.githubusercontent.com/68957257/200525713-73fbd2bf-79f8-4398-aa72-81da8559e003.png">


You will have to [**generate a new SMIBIOS**](https://github.com/corpnewt/GenSMBIOS) before login to your iCloud account.
Bios Gen iMac19,1

Changes:
1. Remove LucyRTL8125Ethernet.kext.
1. Remove USB Mapping HS02 support for the front panel USB-C port.
1. Add USB Mapping HS04 for USB port on the motherboard which used by BCM943602CS with PCI-E&Onboard-USB.
1. Change SMIBIOS to iMac19,1.
