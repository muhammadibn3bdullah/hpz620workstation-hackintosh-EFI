# 🍏 OpenCore EFI for HP Z620 Workstation

This repository contains the OpenCore EFI folder used to successfully run macOS on an HP Z620 Workstation. I have recently transitioned my main workflow to **CachyOS**, but I am open-sourcing this stable EFI configuration for reference and to assist others in the Hackintosh community.

## 👨‍💻 Author
**Muhammad ibn 3bdullah**

## 💻 Hardware Specifications
* **Machine:** HP Z620 Workstation
* **CPU:** Intel® Xeon® Processor E5-1660 @ 3.30 GHz
* **GPU:** Originally an AMD Radeon RX 580 2048SP. **Note:** This specific card was flashed/modified to an RX 570 firmware to ensure full compatibility and hardware acceleration within macOS.
* **RAM:** 32GB ECC DDR3
* **Storage:** 2x 1TB SSD
* **Audio:** Integrated Intel/Realtek HD ALC262 Audio, optional HP Thin USB Powered Speakers
* **Network:** Dual integrated Intel LAN; Infineon TPM 1.2 Controller; Optional Broadcom NIC; Optional Intel NIC

## ⚙️ BIOS & Network Configuration Note
* **Important:** The standard (top) Ethernet port has been **disabled** directly from the BIOS.
* **Only the bottom Ethernet port (labeled AMT)** is enabled and used for network connectivity in this configuration.

## 💿 Supported macOS Versions
* macOS Sequoia (15.x)
* macOS Tahoe / Sonoma (14.x)

## ⚙️ Kexts Included
* AMFIPass.kext
* AppleALC.kext
* ASPP-Override.kext
* CryptexFixup.kext
* CtlnaAHCIPort.kext
* IntelMausiEthernet.kext
* Lilu.kext
* RestrictEvents.kext
* SATA-unsupported.kext
* SMCSuperIO.kext
* USBToolBox.kext
* UTBMap.kext
* VirtualSMC.kext
* VoodooPS2Controller.kext
* WhateverGreen.kext

## ⚠️ Important Disclaimer
**Do NOT** use this EFI as-is without generating your own SMBIOS data. 
You must generate your own `SystemProductName` (e.g., MacPro6,1 or iMacPro1,1 depending on your specific setup), `SystemSerialNumber`, `MLB`, `SystemUUID`, and `ROM` before booting. Using this EFI with empty or duplicate SMBIOS data can lead to Apple ID blacklisting.

This EFI is provided for educational purposes. I am not responsible for any hardware damage or kernel panics. Always refer to the official [Dortania OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/).

## 🐧 The Next Chapter
Currently diving deep into Linux realms, optimizing workflows, and tweaking Arch-based distributions like **CachyOS** for specialized security workflows and penetration testing.
