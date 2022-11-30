# A list of things useful to owners of the GPD Win Max 2

# A check list of things to check on a new device
###### Credits to SuperSexySoapTurtle#6606 on discord.
1. Test gpu under load for black screen. (Use graphically heavy games, 3dmark, photoshop, etc.)
2. Check bios version to make sure its up to date (Only update if necessary, see #1)
3. Test all keyboard keys (A lot of people are having issues with missed inputs) If you're having issues, try putting tape under the keycap
4. Test analog deadzones and update firmware if needed
https://www.mediafire.com/file/2lqucxtobzk0wfc/GPD_Gamepad_Firmware_Tool%25288%2529.exe/file
5. Test for static shock (Some dude was getting shocked by his unit occasionally lmao)
6. Look for dead pixels
7. Test if micro sd & sd card can be read. A lot of users were having issues with it disconnecting and reconnecting. This problem doesn't immediately show up, so if you use  SD and Micro SD a lot, I would monitor this.
8. Touch screen deadzones. Make sure all corners of the screen can be touched correctly. (I'd recommend touching and dragging each corner on the desktop to test this)
9. Make sure touch pad isn't going insane. (If it is, install firmware update from gpd) https://drive.google.com/file/d/1QlJEQPft1qemrM8F5jseteMwCc7-kVY_/view
10. Make sure screen is glued correctly (Some dude could see into his unit through a gap in the upper half of the screen lmao)
11. Do a full scan for malware with Microsoft defender. It should catch whatever worm or virus if any. Or just reinstall OS if you aren't lazy like me.
12. Test analog stick circularity. (https://gamepad-tester.com/)
13. Make sure keycaps don't have cracks in them.
14. Make sure Dpad is working correctly.
15. Make sure remote play is working correctly. (A user was having issues with the screen randomly going black and having to force the machine to shut down.)

# Tools:
1. AMD Software: Adrenalin Edition(https://www.amd.com/en/support)<br/>
2. Driver pack from GPD(https://drive.google.com/file/d/161AkrveUcKXvo2ZEnsnmK-NPVLaCbc7r/view?usp=sharing)<br/>
3. Windows 11 21H2 with inclued drivers from GPD(https://drive.google.com/file/d/1PXQXYhxqyNU3t-T-MWH4cnsPz32KuHID/view?usp=sharing)<br/>
4. WIN Max 2 grip customization tool(https://www.gpd.hk/filedownload/88995)<br/>
5. MotionAssistant(https://discord.com/channels/243411108940087297/826965330965430272/1037625013441933382)<br/>
6. GamePad Test Calibration Tool V1.02(https://www.gpd.hk/filedownload/89292)<br/>
7. Power Control Panel(https://github.com/project-sbc/Power-Control-Panel-v2)<br/>
8. GPD Gamepad Firmware Tool V3.09/V1.21 (https://www.mediafire.com/file/2lqucxtobzk0wfc/GPD_Gamepad_Firmware_Tool%25288%2529.exe/file)<br/>
9. Script for adding extra resolutions and refresh rates(https://discord.com/channels/243411108940087297/802730777443958824/1040061390158827650)<br />
10. Performance overlay for WM2(https://discord.com/channels/243411108940087297/826965330965430272/1045420389368594472)<br/>
11. WM2 Bios files(https://discord.com/channels/243411108940087297/826965330965430272/1040093726380396554)<br/>
12. Ciphray's TDP bat menu(https://discord.com/channels/243411108940087297/826965330965430272/830845629978247209)

# Useful information
1. For chargers, it MUST support AT LEAST PD3.0 15v 3A to trickle charge, but the OS might force your TDP down when plugged in to a charger like that to try to ensure the battery gets charged, a charger that support 20v is heavily recommanded for use while the device is under load(eg. gaming while plugged in), 20v 3A is good enough to play games and charge at the same time, but with a 20v 5A charger and e-marked cable it will be faster if the TDP is high and you are loading the device heavily.

# Known issues
1. Some specific charger would cause the WM2 to lower its TDP when plugged in.
2. On some units the SD card slots will constantly disconnet and reconnect rendering it unuseable.(See below for workaround)
3. Display out on hubs plugged into the USB 3.2 slot doesn't work and lock the resolution to 800x600

# Workarounds
###### SD card slots disconneting constantly workaround, credits to ciphray#8122 on discord for the workaround, credits to Xryptic#5251 on discord for the instructions.<br/>
For anyone having SD/MicroSD disconnect/reconnect issues, the wonderful Ciphray has found a temporary solution that will work until GPD comes up with a fix. It lowers your SD readers speeds to USB 2.0 speeds, but they will stop having problems.

1. Shut your WM2 down
2. Boot and press delete until you enter the bios screen
3. Hold ALT and press F5 to see advanced BIOS
4. Go to Chipset > South Bridge > SB USB Configuration > USB1 Ports
5. Change XHC1 Port 1 to “Disabled”
6. Save and exit BIOS

# Unlock higher than 28W TDP
1. <b>DO IT AT YOUR OWN RISK </b>
2. Go to bios by pressing del key during start up process
3. While in bios menu, press ALT+F5 to access the hidden menu
4. Navigate to the following path Second Advance-> AMD CBS-> SMU Common Options
5. Change the values as follow or to the TDP you want, value is in mW
![Advanced Menu.](/img/cpu_oc_1.jpg "Advanced Menu")
6. Go to the SmartShift Control menu, and set it as follow
![Advanced Menu.](/img/cpu_oc_2.jpg "Advanced Menu")
7. Press ESC to get to the main menu, go to Save & Exit, and select Save Changes and Exit, and then select Yes, machine will reboot, and overclock profile will be set.
