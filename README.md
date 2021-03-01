# Asus-G750JX
Guide and Files to support MacOS Catalina and Big Sur
1) Go to Asus Laptop Bios Setup change under USB, XHCI Pre-Boot Mode from Smart Auto to Enabled or you won’t be able to boot USB installer. Change Launch CSM to disabled this will also disable PCE.
2) create a USB installer of macOS Catalina or Big Sur.   You need pre existing MacOS or friends computer to get a copy
3) Format USB to GUID HFS Journal.   Name USB untitled in order for step 4 to work
4) Make sure a copy of macOS Catalina or Big Sur is in your applications and run this terminal command with USB inserted in step 5.  WARNING If your Windows Hard Drive is labelled Untitled then change the USB to another name and then change Untitled to whatever the name is of your USB in step 5.  This will take a little while to install Mojave onto USB.
5) https://support.apple.com/en-us/HT201372
6) Install Clover v5122 onto USB. IF you are going to install Big Sur you must use CLover v5130 or greater and its a completly different configuration I havenot done you will need to read up on it if you plan on using Clover.  I would stay with OpenCore.
7) install Clover Configurator and use the Mount EFI on located on left side to mount USB
8) Unzip EFI.zip and Copy that folder inside the mounted EFI of USB.
9) Open Clover.plist using Clover Configurator and click on boot left side change Default Boot Volume to whatever name you will give your Mojave Hard drive to.  I named mine MacOSX as you will see.  This step is important because during the install you will get at least 1 or 2 reboots and you want the installer to continue with the correct default hard drive partition or you will manually have to choose it when you boot to clover GUI.
10) Reboot and you may have to click on the ESC key in order to choose your USB drive, but choose the EFI choice USB not the other USB non EFI
11) After installation and boot to desktop you now need to install Clover onto this hard drive but this time choose the Desktop hard drive to install.  SEE CLover SSD or Hard Installer Screenshots.
12) Now mount Hard Drive or SSD EFI using Clover configurator and copy my extracted EFI.zip into the EFI mounted drive replacing the EFI folder inside just as you did for the USB.
13) Once on your Desktop mount SSD EFI again and go to EFI for future updates use Kext Updator app to keep everything up to date.
14) Copy HWMonitor to Applications.  You can leave this copy in Other won’t hurt anything.
15) Run kext cache from Hackentool if needed in order to get your LCD brightness to work after 1 or 2 reboots.
16) Unzip and install VoodooHDA.prefPane-289.  Mac Security may complain about installing this so just go to System Preferences, Security, and click Open Anyways then open again.
17) You can install Gatekeeper from Hackentool
18) Audio stopped working since High Sierra so you are using VoodooHDA and it works better than original Native APpleHDA because you can now control the two sets of speaker Volumes separately.
19) Create a Multi-Output Device from Utilities, open Audio MDID Setup, click on the + at bottom left and create Multi-Output Device then tick both Speaker’s (Analog), I let it tick the one speaker Drift Correction you may have to experiment with this if you have any delays from one speaker versus the other.
20) you have a 100% working MacOS Clone that in my opinions still runs better than any MacBookPro with this processor.
21) GPU works natively.
22) I have included several up to date Apps you can use and Clover Configurator a must for now, also included Plist Editor Pro will only work after you run the gatekeeper command then manually install it that comes with plist Editor Pro.  I also included Ioregistry Explorer used to determine what is working and what is not but everything is working.  I have 5 of these Asus G750JX laptops and they all run Catalina 10.15.6 flawlessly.

These instructions are for an older version of CLover, I have moved to OpenCore so instructions need to be updated when I have time.
Screentime in System Preferences but Sidecar not there.  This is the orignal Asus Azurewave that is still supported buty obviously not all features are supported.
