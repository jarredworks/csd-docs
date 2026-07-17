# DOFLinx
Official DOFLinx Webpage: https://doflinx.github.io/docs/index.html
## What is DOFLinx?
According to the creator of DOFLinx, DDH69, “DOFLinx is pinball and arcade ‘middleware’. It runs on your cabinet, monitoring events from the game emulator and then translates those into cabinet actions.”

Here at CSD, a lot of our hardware is used with DOFLinx to provide haptic feedback, ALED feedback, and SSF support for virtual pinball and arcade emulators. CSD acknowledges that we are not the creators or maintainers of this software and are incredibly grateful for the hard work that many have put forward in service of the community. I highly recommend you check out DDH69’s content and send him support for the creation and upkeep of DOFLinx, to which he continually contributes.
- To support the creator DOFLinx and encourage maitainance and updates, visit this link from his website: https://www.paypal.com/donate?hosted_button_id=YEPCTUYFX5KDE

DOFLinx listens to the game controller/keyboard inputs that are sent to the PC/Emulator. The PC/Emulator then creates signals in-game from the pinball rolling around or other in-game events. DOFLinx interprets this information back to the control board and send the necessary signals to activate the haptic feedback toys. CSD’s products are like a game controller; DOFLinx is a listener and interpreter. Your PC/emulator is where the game is.

Because CSD is not the creator of DOFLinx for the most current information and most all-encompassing guides for unique setups, I recommend checking out the DOFLinx official webpage. This is where I learned to set everything up in DOFLinx! Additionally, there are tons of posts on different forums or platforms such as VPForums, VPuniverse, Reddit, Discord, and YouTube that all helped as well. The goal of this guide is to demonstrate a single configuration for CSD products with DOFLinx as a template for the builder to work from. Because everyone has different setups and requirements, this guide will be limited, and **it will be necessary for the builder to create their own custom configuration**. That said, there is plenty of information, posts, videos, and helpful people there for your assistance on the previously mentioned forums and platforms.
## Goal of this Guide and Parts Used
What will follow is a demonstration and template for builders to get an idea of how to configure DOFLinx to work with a Windows 11 based 3-screen widebody virtual pinball cabinet with a CSD Extreme Builders Kit (x10 solenoids and 4.1 SSF Kit) with the inclusions of a knocker kit, 7 panel ALED Kit, speaker rings, and strobes.

1. PinOne Builders "Extreme" Kit: https://www.clevelandsoftwaredesign.com/pinball-parts/p/virtual-pinball-builders-kit. The items included and method of hookup are detailed in this video: https://www.youtube.com/watch?v=5BLjU5GOnZk&t=6s.
2. Addressable LED Kit: 
    - For this configuration I used:
      - The ALED Kit with 7 matrix panels
      - Total ALEDs: 2 strips (JP1-2), 7 panels (JP3-9), x2 daisy-chained speaker rings (JP10). JP1-10 refers to the physical ports on the ALED controller.
3. 4.1 SSF System


- TESTING and ASSEMBLY Instructions:
  1. Builders Kit: https://www.youtube.com/watch?v=5BLjU5GOnZk&t=6s
  2. ALED Kit: https://www.youtube.com/watch?v=RJ985EQpjYI&t=127s
  3. SSF Kit: https://www.youtube.com/watch?v=TXzHTG9J9_0&t=39s

Any files and configurations that follow will be specifically for CSD products and the specific build that I mentioned directly above. If you are imitating this exact build, then great! You may be able to just take the ones below and be done! If you are running another build, then hopefully this points you in the right direction!

Note, this installation and configuration is performed on a PC that has installed and working: DOF, PinUp Popper Baller Installer, Terry Red’s Future Pinball and BAM AIO, and Steam. This is how I got it to work with my PC and setup, but installation and configuration may be different for each builder. 

## Warning
Warning from the creators of DOF and CSD: This software has been designed to control hardware which is connected to a computer. This means that there is always a risk that something goes wrong and that your hardware or something else gets damaged. You use this software at your own risk! Dont blame me if your boards go up in smoke, your house burns down or something or someone else gets damaged. You have been warned!

Finally, before proceeding with the configuration, I again recommend carefully reading through the official DOFLinx webpage that the builder may understand what DOFLinx is, the requirements for DOFLinx, and a foundational understanding of how DOFLinx may be configured. 

## Additional Resources and Community Guides

TerryRed Install and Configuration Guide: https://www.youtube.com/watch?v=OrXP4CLSmkg&list=PLLw6pcnEfiyP50Yb4hEFLFCV8ziYZCkYI&index=14&t=1261s

***TerryRed's guide may be the best in-depth installation and configuration guide that I know of for DOFLinx. It is due to TerryRed’s efforts and guides that I was initially able to use DOFLinx at all!***

Install guides:
DOFLinx wiki: https://doflinx.github.io/docs/index.html

VPforums: https://www.vpforums.org/index.php?showtopic=36184

Getting FX to work: https://doflinx.github.io/docs/getting-started/06_PinballFX.html

Enabling SSF: https://doflinx.github.io/docs/getting-started/11_SSF.html

Nudge Guide/Forum: https://www.vpforums.org/index.php?showtopic=42325&page=1

Doflinx effects guide (for making sup ini for other games w/o premade doflinx support):https://www.vpforums.org/index.php?showtopic=41576

# CSD's DOFLinx Install Guide
## Initial Requirements
- PinUp Popper Installed and Functioning
- DOF Installed and Functioning (check out our other tutorial!) *This step is necessary!
- Other Requirements: https://doflinx.github.io/docs/getting-started/02_Requirements.html

## Step 1: Download DOFLinx
1. Navigate to the official DOFLinx webpage (https://doflinx.github.io/docs/index.html)
2. Under the “Getting Started” Tab, select the “Installation” subtab.
3. Select the link (https://github.com/DOFLinx/DOFLinx/releases) in "step 2" and download ZIP file of the latest version of DOFLinx from GitHub. (At the time of release, the latest release is “DOFLinx_V916.zip”.
4. In File Explorer, unblock “DOFLinx_V916.zip” by right-clicking on it and selecting “Properties”.
    - In the properties page check “unblock” then “apply”.
5. In File Explorer, extract “DOFLinx_V916.zip” using 7-Zip by right-clicking on it and selecting open with 7-Zip. Then extract the files.
6. Open the newly created folder DOFLinx_V916 and copy all of the contents in this folder.
7. Paste the contents of DOFLinx_V916 to your DirectOutput Folder.
8. The final result should look like this:

INSERT IMAGE

## Step 2: DOFLinx.vbs for Future Pinball
1. In the DirectOutput folder, copy DOFLinx.vbs.
2. Paste DOFLinx.vbs in the Scripts folder your Future Pinball Folder.
    - The file path for the location of the DOFLinx.vbs will be

      INSERT FILE PATH

## Configuring the DOFLinx.ini file
This step is crucial because it is essentially telling DOFLinx what devices and toys you have so that they may be activated and controlled. 

IF YOU ARE USING AFOREMENTIONED BUILD/HAVE THE CSD EXTREME KIT (Main Board):
Here is a sample DOFLinx.ini file for the build that I have mentioned:
Paste this file in your DirectOutput folder and replace it with the old DOFLinx.ini file. 

INSERT FILE


IF YOU HAVE THE CSD VR CABINET KIT (Mini Board):
Open “sample.ini files” 

INSERT FILE


IF YOU HAVE A MINI MACHINE:

INSERT FILE


If you have an alternative setup or a differing setup, I recommend you check out the “Sample INI files” folder in your DirectOutput folder and use the “DOFLinx- Almost Everything TerryRed update.ini”. You will personally need to edit and rename this fine before placing it in your DirectOutput folder. TerryRed has done a lot of explaining the specific in this file and has have a video (https://www.youtube.com/watch?v=OrXP4CLSmkg&list=PLLw6pcnEfiyP50Yb4hEFLFCV8ziYZCkYI&index=15&t=1261s) which walk you through this process (for cabinets, use minute 35:20).

## Step 4: Allow DOFLinx in ShellStartup
1. In your DirectOutput folder, copy “DOFLinx-Shortcut.lnk”
2. Open the startup folder in Windows by pressing Win-R (Windows button and R at the same time) and typing in shell:startup
3. Paste DOFLinx-Shortcut.lnk in your startup folder. DOFLinx will now activate when the computer is turned on.
4. Reboot your PC and see if it works!
