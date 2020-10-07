# Opencore-IvyBridge-H61-Motherboard
IvyBridge Hackintosh based on OpenCore 0.6.1 - Gigabyte H61 Motherboard. 
------------------------------------------------------------------------
Successfully installed Mac OS Catalina 10.15.7 on an Gigabyte H61 Motherboard using the opencore 0.6.1 bootloader.
Followed the steps mentioned in this guide: https://dortania.github.io/OpenCore-Install-Guide/

System Specifications:
=====================
1. CPU i5-3340 Quad core Processor with stock Intel cooler.
2. Gigabyte H61-MS MotherBoard.
3. Ram 6GB (4GB + 2 GB). Will be upgrading to 8GB RAm.
4. Seagate 1 TB HDD.
5. GPU: Nvidia GT 710 2GB graphics card.
6. Circle 500W PSU.
7. Zebronics PC Cabinet.
8. Logitech USB Keyboard + Mouse Combo.
9. AOC 21.5 inch LED Monitor. (Even connected 32 inch LG LED TV in extended display mode).
10. V-Guard 600VA UPS.

What's Working?
===============
1. Hardware acceleration fully supported (Intel HD Graphics 2500 in headless mode).
2. Sleep/Wake.
3. Restart.
4. Shutdown.
5. Internet(RTL8111 kext)
6. Audio (used layout id -5, can use layout id -11 [Headphones default selection]). Depends upon on motherboard audio codec, mine is Realtek ALC 887 Codec.
7. USB.
8. Nvidia GT 710 2GB DDR3 (Out of Box Supported).
9. DRM functioning successfully (Apple TV, Amazon Prime, Netflix videos are playing fine).
10. Icloud services (iMessage, Facetime, etc). To get this work you need a good serial number. <b>I have removed the serial used from the config.plist file due to security reasons. You can update your own serial and ROM (use your ethernet MAC address without any : or - seperation). Use GenSMBIOS https://github.com/corpnewt/GenSMBIOS.</b>
11. Power Management.

What's Not working?
==================
Everthing seems to be fine. No problems discovered so far.

All required SSDT files are added in ACPI folder. <b>I recommend to regenerate the SSDT-PM for your processor during post install (The processor used is i5-3340).</b>  

One Important recommendation to get iCloud services to function properly: <b><i>Use an Apple ID which is already linked to one of your Orginal Apple Devices.</i></b> (This can avoid your Hackintosh getting blacklisted).

Tools used:
==========
1. ProperTree. https://github.com/corpnewt/ProperTree (used on Windows 10 & Mac OS Catalina) 
2. GenSMBIOS. https://github.com/corpnewt/GenSMBIOS   (used on Windows 10 during Pre build time)
3. Pike's ssdtPRGen.sh. Used for generating SSDT-PM (CPU Power Management SSDT). I followed this guide for SSDT file generation. https://www.elitemacx86.com/threads/guide-how-to-generate-ssdt-for-cpu-power-management.96/. Used during Post Install in Mac OS Catalina 10.15.7.
