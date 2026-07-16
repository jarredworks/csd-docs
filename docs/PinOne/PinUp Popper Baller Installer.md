---
sidebar_position: 1.23
---
# PinUp Popper and PinUp Popper Baller Installer
*PinUp Virtual Pinball System is NOT a system created or maintained by Cleveland Software Design. PinUp Virtual Pinball System was created and is maintained by Nailbuster Software. I highly recommend you go [support]([url](https://nailbuster.com/wikipinup/doku.php?id=donate)) them for the great community service they provide for the Vpin world! Cleveland Software Design is not responsible for the maintenance or setup of any individual user’s download of any PinUp system. This documentation is meant only to be a free guide for a specific VPin build (3-screen cabinet build detailed in the other CSD tutorials). As a community, feel free to use this guide as a template for your own builds!

Before beginning, I HIGHLY recommend you check out and completely read through all of the PinUp Virtual Pinball System Wiki website. PinUP Wiki has most everything you need to get started and configure the system for your specific needs or requirements. Everything from installation, settings, controller configuration, emulators, adding games, updates, etc. is all on PinUp Wiki website. Please, use this resource and frequently check it, for it will be a great help to you!

Official PinUp Virtual Pinball System Wiki: https://nailbuster.com/wikipinup/doku.php?id=baller_installer
## Support for the PinUp System can be found at these links:
Community Help via Discord Virtual Pinball Chat Group: http://bit.ly/virtualpinball

Community Help via Baller Installer FaceBook group dedicated to this installer: https://www.facebook.com/groups/138794908064016

Help with AtGames Legends Pinball: http://wagnerstechtalk.com/alpbi/

A great quick reference diagram by Dux Retro: https://tinyurl.com/VPFolderInfo

Website to help find all the great community content: https://virtual-pinball-spreadsheet.web.app/

To see a list of community sites and project links for latest info see here: https://www.nailbuster.com/wikipinup/doku.php?id=contributors
## Nailbuster's Tutorials and other great community tutorials:
Nailbuster's Install Tutorial: https://www.youtube.com/watch?v=nyZ2s4jw--8

Nailbuster's "After you get it running/installing games" tutorial: https://www.youtube.com/watch?v=dOLBgO1jmko

Terry Red's Tutorial: https://www.youtube.com/watch?v=nI8wD4Pwvfg

Rudy’s Arcade's Tutorial: https://www.youtube.com/watch?v=SPW7fO5vA-k&list=PLLw6pcnEfiyP50Yb4hEFLFCV8ziYZCkYI&index=8

## What's Included In PinUp Popper Baller Installer?
- Visual Pinball X(VPX) 10.8.0 Release Candidate 5  Build # 2028 (x64 GL/DX) & v10.7.4
- PinUP Player v1.5 (latest)
- PinUP Popper FrontEnd v1.5 (latest)
- VPINMAME 3.6.0-sc (build 1167) x86/x64
- B2s-Backglass Server v2.1.2 (32/64bit)
- FlexDMD v1.9.1
- DMD-Ext (freezy) v2.3.0 (32/64bit)
- Future Pinball w/BAM (latest and greatest)
- TerryReds PinEvent FP system
- Two original tables: ScottyWics "Leprechaun King" and
- TerryRed's "Retro Flair BAM Edition"

//**latest as of Jan /2025 (run PinUPdater to get latest versions afterwards)**  //

## What's NOT Included?
- DOF (Direct Output Framework For VP And some FP)
- DOFLinx (For FX2 & FX3, FP And Mame)
- UltraDMD (uses FlexDMD instead as that is the suggested replacement today)
- FutureDMD / FPIntercept (realdmd for some future pinball)
- drivers for hardware like pinscape, pin2dmd usb driver, pindmdv3 dlls. (outside of dmdext/freezy support)

*DOF is not included in Baller Installer, but was created by another team. DOF handles haptic feedback toys such as we have available on Cleveland Software Design’s website for VPinball and MAME. These toys include solenoids, knockers, shakers, control boards, ssf, addressable leds, etc. Check out our website for more information! I highly recommend an [Extreme builders kit]([url](https://www.clevelandsoftwaredesign.com/pinball-parts/p/virtual-pinball-builders-kit)) which will be used for this tutorial series.

## What if I mess up and need to start over?
If you need to start over for any reason whether it be weird settings that you can’t fix, display issues, file paths, etc. I recommend using Rudy’s Arcade’s guide on preparing for a fresh install: https://www.youtube.com/watch?v=SQrNqoPULL4&t=2s

# CSD PinUp Popper Baller Installer Guide
Initial Requirements
- Windows 10/11. This guide will be using Windows 11. 
- PC and 3 Monitors already installed and connected to each other.
- Patience to read all of the documentation on the PinUp Wiki and this guide without skipping anything.
- Patience with yourself and your PC.
- Courage to use the support groups mentioned before.
## Step 1: Set Up Displays
It is crucial to set up displays properly before running baller installer. I personally had a lot of issues in the past with displays that were due to doing this out of order. 

Navigate to “Display Settings” in your Windows Settings and ensure the display settings are as follows: 
- Landscape
- Scale 100%
- Resolution (I recommend the highest supported resolution of your PC/monitors, or the recommended resolution)
- Multiple Displays (Remember I have 3 displays→ playfield, backglass, dmd)
- Make your playfield monitor primary
- Toggle “multiple displays” on if off
  - Line everything up
  - From left to right your displays should be: Playfield→Backglass→DMD
  - Order of numbers does not matter
  - Displays MUST be in a straight line across the top. The tops of the screens must all line up.
  - Reboot the PC and ensure the screen settings are correct. 
<img width="502" height="508" alt="Screenshot 2026-06-17 at 10 38 41 AM" src="https://github.com/user-attachments/assets/71803d3a-1c64-4bc6-ac8b-a4968b387bf9" />

## Step 2: Turn off antivirus software
I recommend turning off antivirus software before installing so that Windows doesn’t restrict or block anything. You can turn on antivirus software after the installation is done, but it is recommended to place the “Visual Pinball” folder in the “Exclusions” section of the antivirus settings.

Do so at your own risk! A designated VPinball PC is still concerning, but having these turned off on a personal computer can be a huge risk. Do not blame CSD if you get malware!

1. Navigate to the “Virus and Threat Protection” settings in Windows
2. Select “manage settings” for Virus & Threat Protections Settings and switch the following to off:
   - Real-time protection
   - Dev Drive Protection
   - Cloud-Delivered Protection
   - Automatic sample submission
   - Tamper Protection
## Step 3: Download PinUp Popper Baller Installer
1. Make sure you are connected to the internet for the duration of the installation.
2. In your internet browser search for “PinUp Popper Baller Installer” and navigate to Nailbuster’s website. I recommend you read all the information on the PinUp Wiki, especially the starting page and the install page. This will clarify things and save a lot of headaches if you get stuck.
3. Navigate to the “Download Installer” heading and download the most recent version.  Your browser will likely flag the download and ask you to keep it once fully downloaded.  Press the 3 dots (More actions) and select “keep”. “Make sure you trust PinUp_Popper_Baller_Installer…exe  before you open it”. Press the down arrow Press “Keep anyway”
4. Open File Explorer
5. Unblock the installer application
6. Find the download. Should be something like “PinUp_Popper_Baller_Installer…exe”
7. Right click
8. Navigate to properties
9. Select Unblock
10. Select Apply
11. Run the Application
12. If it asks, allow it to make changes to the device.
<img width="887" height="687" alt="Screenshot 2026-06-17 at 10 59 51 AM" src="https://github.com/user-attachments/assets/50bde182-9834-4789-b7c7-135ec3841040" />
<img width="158" height="208" alt="Screenshot 2026-06-17 at 10 39 27 AM" src="https://github.com/user-attachments/assets/391606fa-02b9-48cf-8690-28d6004e6dd0" />

## Step 4: Set Up
1. License Agreement
2. Select “I accept the agreement”
3. Next
4. Select Destination Location
5. Leave it as whatever the default location is. At the time of this guide, it is “C:\vPinball”
6. Next
7. Ready to Install
8. Select “Install”

At this point, the installation will begin. There may be a few programs that open up; ignore them until the installation is complete. 
Leave “Set Up- PinUp Popper Baller Installer…” open for this next part.
<img width="582" height="456" alt="setup- pinup popper baller installer" src="https://github.com/user-attachments/assets/7ac8cf69-e7a6-488d-a5f1-602d8f89062c" />

## Step 5: DirectX
At the end of the “Set Up” Installation, DirectX will appear.

1. Select “I accept the agreement”
2. Next
3. DirectX Runtime Install
4. Next
5. DirectX will then install…
6. Installation Complete
7. Finish
<img width="872" height="648" alt="Direct X" src="https://github.com/user-attachments/assets/83bc8cf8-1408-495a-9538-ddda1f18a898" />

## Step 6: “Set Up- PinUp Popper Baller Installer..”
“Completing the PinUp Popper Baller Installer Setup Wizard”
1. Make sure run config is checked.
2. Finish
3. “Set Up- PinUp Popper Baller Installer…” will close.
<img width="596" height="466" alt="Setup- run config" src="https://github.com/user-attachments/assets/9fd3e985-8c45-46b9-956d-8e52fad8004f" />

## Step 7: PinUp Popper Baller Installer
1. Intro
   - Next page
<img width="1203" height="766" alt="Screenshot 2026-06-17 111002" src="https://github.com/user-attachments/assets/e0d31c40-a9fc-4169-9ce9-1ccb08d1f3f1" />

2. Set Layout
   - Select your layout
   - Layout C (FullDMD)
   - Playfield Resolution
   - 4K 2160p
   - Apply Layout
<img width="1151" height="759" alt="pinup popper baller installer- set layout" src="https://github.com/user-attachments/assets/54bc47ce-60a0-4636-a5b4-df8426ec0594" />

3. Help
   - Check Windows “Display” Settings again.
   - Next page
4. Config/Install (This portion has laid out steps that will guide you through).
  - Step 1: Test Display Layout
  - Step 2: Install Apps. Apps will open and close. Ignore them.
  - Step 3: Setup Display Positions
    - Topper
      - Drag to the top of the DMD, even if you don’t have one.
    - Slim DMD
      - My build is using a full DMD, but it is still necessary to drag it over to the bottom of your DMD.
    - Backglass
      - Drag to backglass screen. Select “full screen”.
    - Playfield
      - Make sure it is on you playfield screen. Select  “full screen”. If your setting menu gets covered click “show select” to get it back.
    - Music
      - Drag to DMD and select “full screen”
    - Apron/FullDMD
      - Drag to DMD and select “full screen”.
  - Save settings
  - Exit Setup
  - Step 4: Apply Display Settings to all Apps
    - Next Step- DMD Page
<img width="1184" height="757" alt="pinup popper baller installer- config install" src="https://github.com/user-attachments/assets/5f5554cc-fd38-47b0-8687-982137074f67" />
<img width="1165" height="835" alt="Screenshot 2026-06-17 111408" src="https://github.com/user-attachments/assets/b9c109a0-d7d1-4028-98e7-648b2c70169e" />

5. Real DMD
   - Select FullDMD
   - Ensure it is in the correct position.
   - Select Show Backglass
   - Ensure it is in the correct position.
   - Test DMD
   - Drag it to the correct position.
   - Resize (Not a huge thing to worry about right now, DMD can and will be adjusted later.)
   - Save DMD settings
   - Right click and “save globally”.
   - Stop Test
   - Next Page
6. All Done
- You're all done with the install!
## Step 8: Checking for PinUp Popper Updates
1. Open the “PinUp” Folder that is now on your desktop.
2. Open “PinUp Popper Config”.
3. Press the globe icon in the right-hand corner.
4. Ensure all PinUp apps are closed and you are connected to the internet.
5. Select “yes”.
6. PinUpDater
   - Select “check for updates” in the right hand corner.
   - Select “apply updates” in the right hand corner.
   - Once finished select “OK”.
<img width="693" height="420" alt="pinuppoppersetup-checking for updates" src="https://github.com/user-attachments/assets/e6ec758b-7987-49a7-8b8a-712d22f2aae6" />

## Step 9: Turning Antivirus back on and adding exclusions
1. Navigate to the “Virus and Threat Protection” settings in Windows
   - Under Virus & Threat Protections Settings select “Add or remove exclusions”
   - Select “add an exclusion”
   - Select “folder”
   - Naviage to “C:” (often “this PC” → “windows (C:)”
   - Select “vPinball” Folder
   - Do the same for the “PinUp” Folder
   - Located on the desktop
2. Under Virus & Threat Protections Settings switch the following to on:=
   - Real-time protection
   - Dev Drive Protection
   - Cloud-Delivered Protection
   - Automatic sample submission
   - Tamper Protection
## Step 10: Enjoy!
Run “PinUp Popper Front End” in the PinUp Folder to play!

# What’s Next?
- Enjoy the free tables included!
- Controller Set up
  - Configure PinOne as a controller to navigate in PinUp Popper Front End
  - Configure PinOne as a controller with VPX
- Download more tables
  - Find tables online and add them to your system.
- Launch Future Pinball in the PinUp Folder to ensure it is functioning.
  - File
  - Open table
  - RetroFlair
  - Play table
- Adding media for downloaded games
- DOF/DOFLinx
  - Haptic Feedback systems, if you have haptic feedback toys
  - NOT included in PinUp Baller Installer
  - Separate applications that need to be downloaded and configured
  - Check out our other tutorial!
