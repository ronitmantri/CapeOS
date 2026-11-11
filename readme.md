# CapeOS

### How to install for Raspberry Pi: 
What you need
A Raspberry Pi 4 or 5 (a Pi 3 works but is slower), a microSD card (16 GB or more), and a power supply.
A monitor with an HDMI cable, plus a keyboard and mouse.
The CapeOS-RaspberryPi.zip file I gave you.
Part 1: Put Raspberry Pi OS on the SD card (same on Windows and Mac)
Download Raspberry Pi Imager from raspberrypi.com/software and install it.
Insert the SD card into your computer.
Open Imager, then choose:
Device: your Pi model.
OS: Raspberry Pi OS (64-bit), the one with desktop.
Storage: your SD card.
Click Next, then Edit Settings and set:
A username and password.
Your Wi-Fi name and password.
The option to enable SSH. You only need this if you want to copy the zip over the network (Option B below).
Click Save, then Yes to write the card. Wait for it to finish.
Put the SD card in the Pi, connect the monitor, keyboard and mouse, then plug in power. After a first-boot setup, you’ll see the desktop.
Part 2: Get the zip onto the Pi (pick one)

Option A: USB stick (easiest)

Copy CapeOS-RaspberryPi.zip onto a USB stick on your Windows or Mac computer.
Plug the stick into the Pi. A file window opens.
Drag the zip into the Home folder.

Option B: Over the network (needs SSH turned on)

Windows: open PowerShell, then run:
  scp "$HOME\Downloads\CapeOS-RaspberryPi.zip" yourusername@raspberrypi.local:~/
Mac: open Terminal, then run:
  scp ~/Downloads/CapeOS-RaspberryPi.zip yourusername@raspberrypi.local:~/
Replace yourusername with the username you set. If raspberrypi.local doesn’t work, use your Pi’s IP address instead.
Part 3: Install CapeOS (on the Pi)
In the Pi’s file manager, right-click the zip, then choose Extract Here.
Open the Terminal (the black icon on the top bar) and run these one at a time:
   cd ~/CapeOS-RaspberryPi
   chmod +x install.sh uninstall.sh
   ./install.sh
If it asks for your password to install Chromium, type it. The password won’t show as you type.
When it finishes, open the menu and look for CapeOS, or run ~/CapeOS/capeos-start.
Using it
CapeOS opens full screen. Press Alt+F4 to close it.
To open it in a normal window instead, run ~/CapeOS/capeos-start --window.
By default CapeOS starts every time you log in. Install with ./install.sh --no-autostart to turn that off.
To start CapeOS right at boot, run sudo raspi-config, go to System Options → Boot / Auto Login, and choose Desktop Autologin.
To remove it, run ~/CapeOS/uninstall.sh.
If something goes wrong
“Permission denied” on install.sh: run chmod +x install.sh first.
Blank screen or nothing opens: run ~/CapeOS/capeos-start --window and tell me what the terminal shows.
Port in use: run CAPEOS_PORT=9000 ~/CapeOS/capeos-start.

### A smarter operating system. Privacy by design.

CapeOS is a modern operating system concept built around one idea: combine the best features of iOS and Android into one beautifully designed, privacy-first experience.

Designed to feel familiar, powerful, intuitive, and refreshingly simple, CapeOS explores what a modern operating system could look like without sacrificing usability for aesthetics or privacy.

> **Project status: Demo / Prototype**
>
> CapeOS is currently a demonstration project. It does not install as a real operating system or interact directly with physical device hardware.

---

## Overview

CapeOS aims to rethink the everyday operating system experience.

Taking inspiration from the simplicity and consistency of Apple's ecosystem and the flexibility and customization of Android, CapeOS brings together a unified interface with a strong emphasis on privacy, personalization, and usability.

The project is currently an interactive software demonstration showcasing the proposed interface and functionality.

## Features

### System Interface
- Modern, clean operating system interface.
- Redesigned lock screen.
- Customizable home screen concept.
- Control Center.
- Notification Center.
- Universal search.
- App Library.
- Widget support.
- Multitasking interface.
- Smooth animations and transitions.

### Privacy & Security
- Privacy-first design philosophy.
- Dedicated Privacy Dashboard.
- Centralized privacy settings.
- Clear permission-management interface.
- Transparent system controls.

### Built-in Applications

| Application | Description |
|---|---|
| App Store | Demonstration storefront featuring fictional applications. |
| Settings | Centralized system configuration interface. |
| File Manager | Concept for managing files and folders. |
| Calculator | Built-in calculation interface. |
| Notes | Simple note-taking application. |

### System Features
- Battery dashboard.
- Theme and appearance settings.
- Simulated system updates.
- Boot animation.
- Notification management.
- Device interaction simulations.

### Interactive Demo Actions

CapeOS includes a dedicated Actions panel that demonstrates interactions normally requiring a physical device.

Examples include:

- Plug in phone.
- Unplug phone.
- Simulate charging.
- Simulate battery changes.
- Trigger system notifications.

These actions simulate device behavior
