---
layout: default
title: "IT Help Desk Guides"        # override site.title
description: "Windows 11 Installation Guide"  # override site.description

---

Here is a clear step-by-step guide for installing Windows 11 for the first time. This process will completely erase the drive (including the encrypted data). 

________________________________________

### Check System Requirements

Before installing, confirm the PC meets the minimum specs for Windows 11. [Here](https://www.microsoft.com/en-us/windows/windows-11-specifications?r=1) is Microsoft’s official minimum requirements. 

________________________________________
### Download the Windows 11 Installer

1.	Download the official Windows 11 Media Creation Tool from Microsoft: 
- [https://www.microsoft.com/software-download/windows11](https://www.microsoft.com/software-download/windows11)
2.	Run the Media Creation Tool
3.	Select Create installation media
4.	Choose:
a.	Language
b.	Edition
c.	Architecture (64-bit)
5.	Select **USB Flash Drive (8GB or larger)**
6.	The tool downloads and prepares the installer

This process makes a bootable Windows 11 installer via USB Thumb Drive.

________________________________________

### Proceed to Boot From USB

Here are steps to boot from USB Thumb Drive. 

1.	Insert the USB
2.	Power it on and repeatedly press your boot key:
- F12 (Dell/Acer)
- F9 (HP)
- F10 (some models)
- ESC (ASUS)
- It varies by manufacturer
3.	Choose the USB device

If Secure Boot blocks it, you may need to temporarily disable Secure Boot in BIOS.

________________________________________

#### Delete the BitLocker Partitions (Critical Step)

[Reset your PC](https://support.microsoft.com/en-us/windows/reset-your-pc-0ef73740-b927-549b-b7c9-e6f2b48d275e) is a useful feature that lets you return your device to its original state. It can help resolve performance slowdowns, fix software issues, or provide a clean start. The tool is designed to be easy to use and offers several options so users can choose the reset method that best fits their needs.

However, if the device is inaccessible, fresh reinstallation is required for a PC might be required. Please note that this process will completely erase the drive (including the encrypted data). 

If the drive is encrypted with BitLocker and you do not have the recovery key:
- You cannot recover the existing data
- You must delete the encrypted partitions during installation

If you still need the recovery key, check:
- [https://account.microsoft.com/devices/recoverykey](https://account.microsoft.com/devices/recoverykey)
(If you logged in with a Microsoft account)

When Windows Setup starts:

1.	Click **Install Now**
2.	If asked for a key → click **I don’t have a product key**
3.	Choose your Windows edition
4.	Select **Custom: Install Windows only (Advanced)**

You will now see disk partitions.
This is important:

- Select each partition on the internal drive
- Click **Delete**
- Do this until you see one large block called **Unallocated Space**

This removes BitLocker encryption completely.

________________________________________

### Install Windows

1.	Select the **Unallocated Space**
2.	Click **Next**
3.	Windows will install normally
________________________________________

### After Installation

- Windows 11 license usually activates automatically if:
- It was previously activated on that machine
- The license is embedded in firmware (OEM key)

You do not need the BitLocker key for activation.
________________________________________

### If It Asks for BitLocker Before Booting USB

Some systems show a BitLocker recovery screen immediately on power-on. In that case:
- Enter BIOS
- Change boot order so USB is first
- Or use one-time boot menu key


