# DOF
Official DOF website: https://directoutput.github.io/DirectOutput/index.html

## Initial Requirements:
- PinOne System → Or a kit: Extreme Builders Kit
  - Main Board/Mini Board
  - Power supply
  - Solenoids and Life Extenders
  - Knocker
  - Shaker Motor
  - Light Bar and Strobes
  - Beacons
  - Fan
  - Etc...
- For this configuration, I used the PinOne Builders "Extreme" Kit: https://www.clevelandsoftwaredesign.com/pinball-parts/p/virtual-pinball-builders-kit. The items included and method of hookup are detailed in this video: https://www.youtube.com/watch?v=5BLjU5GOnZk&t=6s.
- Addressable LED Kit: 
  - For this configuration I used:
    - The ALED Kit with 7 matrix panels
    - Total ALEDs: 2 strips (JP1-2), 7 panels (JP3-9), x2 daisy-chained speaker rings (JP10). JP1-10 refers to the physical ports on the ALED controller.
- SSF System (Not needed or controlled by DOF, but highly recommended addition to your build).
- Tested and initial configuration using the PinOne configuration tool
  - PinOne Configuration Tool: https://pinball-docs.clevelandsoftwaredesign.com/docs/PinOne/Configuring/
  - TESTING and ASSEMBLY Instructions:
    - Builders Kit: https://www.youtube.com/watch?v=5BLjU5GOnZk&t=6s
    - ALED Kit: https://www.youtube.com/watch?v=RJ985EQpjYI&t=127s
    - SSF Kit: https://www.youtube.com/watch?v=TXzHTG9J9_0&t=39s
- Windows 11
- Compatible Emulators
  - I recommend using PinUp Popper Baller Installer to get you started! Check out our tutorial!
- A whole lot of patience

## What is DOF?
DOF stands for Direct Output Framework. DOF is a system that serves as a bridge between emulators such as Visual Pinball and physical haptic feedback hardware that is installed into a VPin cabinet. It listens to in-game signals of the emulator and translates them into haptic feedback whether it be solenoids activating on bumpers and flippers, SSF table sounds/ball tracking, or ALED Lights. DOF is what takes virtual pinball from being a game on a screen to a real, immersive arcade experience!

DOF was originally developed by Swisslizard, but has since become open source and has been developed and maintained by the community. Cleveland Software Design did not create and does not maintain DOF; users are responsible for the configuration and operation of DOF if they choose to implement this into their build.

Warning from the creators of DOF (and CSD):

Warning: This software has been designed to control hardware which is connected to a computer. This means that there is always a risk that something goes wrong and that your hardware or something else gets damaged. You use this software at your own risk! Dont blame me if your boards go up in smoke, your house burns down or something or someone else gets damaged. You have been warned!

# Installing DOF
1. Navigate to the PinUp Popper Website in your browser: https://www.nailbuster.com/wikipinup/doku.php?id=baller_installer
2. Navigate to to the “Install” subtab.
3. Scroll down until you reach the DOF R3++ and select the link: http://mjrnet.org/pinscape/dll-updates.html
   - On this page, find the “DOF” heading and use the “Windows setup (.msi)” links to install BOTH x86 and x64 version of DOF.
5. Install x86 (32 bit version) and x64 (64 bit version).
   - At this time, I like to add the DirectOutput folder that has been created to my “exclusions” so that antivirus software doesn’t flag anything.
6. Navigate to the “Virus and Threat Protection” settings in Windows to add DirectOutput folder to exclusions.
   - Under Virus & Threat Protections Settings select “Add or remove exclusions”
   - Select “add an exclusion”Select “folder”
   - Navigate to “C:” (often “this PC” → “windows (C:)”
   - Select “DirectOutput” Folder

# Configuring DOF
1. Create an account on the DOF Config Tool website: https://configtool.vpuniverse.com/app/home
   - I suggest you familiarize yourself with the DOF config tool and the “downloads & links” portion of the Home page. 
2. Navigate to “Manage” under the Cabinets tab.
   - Select “New Cabinet”
   - Name your cabinet
   - Select “create”
<img width="1440" height="776" alt="Screenshot 2026-06-18 at 3 18 42 PM" src="https://github.com/user-attachments/assets/b9387472-48f9-443a-9e3c-d9ebba5c9c83" />
<img width="1437" height="775" alt="Screenshot 2026-06-18 at 3 24 15 PM" src="https://github.com/user-attachments/assets/53a4c1fb-eddb-411c-88cc-b43672d120e5" />

3. Navigate to “Devices” under the Cabinets tab.
   - Select “1” under PinOne.
   - Select “1” under WS2811. (Only if you have addressable LEDs)
     - Note: I am using only these two devices per the set up I have. These two devices covers my PinOne and the ALED kit. SSF is handled separately from DOF.
   - Select “update” to save.
<img width="1440" height="771" alt="Screenshot 2026-06-18 at 3 15 12 PM" src="https://github.com/user-attachments/assets/966f10b2-7452-4f9c-83e7-2c600b5b5a6d" />

4. Creating the DOF configuration in “Port Assignments”/Creating the directoutput.ini files
   - Navigate to the “Port Assignments” subtab under Cabinets
   - Select the device you want to configure
   - You will need to create a directoutput.ini file for each device you are using, so I you will have a total of two directoutput.ini files.
   - Select “device and select “PinOne”
5. Configure “PinOne” as pictured.
   - Select update to save.
<img width="1440" height="777" alt="Screenshot 2026-06-18 at 3 28 43 PM" src="https://github.com/user-attachments/assets/aa62ed50-a97c-4509-b010-203931b8a8aa" />

6. Select “device” and switch to “WS2811”. (This step is only needed if you have addressable LEDs)
   - Configure “WS2811” as pictured.
<img width="1024" height="569" alt="Screenshot 2026-06-18 at 3 39 17 PM" src="https://github.com/user-attachments/assets/8dfebbc3-a590-4965-a9db-a43d950df74e" />

7. Select update to save. 
8. Generating your configuration files
   - Once finished configuring your devices in DOF, you will need to generate two directoutput.ini files, one for the PinOne and the other for the WS2811/ALEDs.
   - At the top right of the webpage select “Generate Config”.
   - The DOF Configuration Tool will then generate a ZIP file containing two directoutput.ini files which will be downloaded to your computer. (Make sure to unblock them if they are blocked). 
9. Placing the directoutput.ini files in the correct file path
    - Unblock and Extract the directoutput.ini files.
    - Once the directoutput.ini files have been downloaded to your computer, you will need to unblock and extract the files in File Explorer.
      - To unblock the files, right click the zipped directoutput.ini folder and select “properties” check the “unblock” box and then select “apply”.
      - To extract the files, right click the directoutput.ini folder and select “7-Zip and Extract”. I am using 7-Zip (a file management software) to extract the zipped files.
    - Place both directoutput.ini files in the “config” folder of the “directoutput” folder.
      - Open the unzipped folder and copy both directoutput.ini files.
      - Navigate to the “directouput” folder and open your “config” folder.
      - In the “config” folder paste the directoutput.ini files.
        - I also recommend pasting the directoutput.ini files in the “x64”, “x86”, and “directoutput” folder. This step is technically unnecessary; however, most DOF issue occur because of on improper file path. This extra step takes a shotgun approach and has the directoutput.ini files everywhere DOF might look for them in case you do mess up the file path.
    - Your file path should look like this:
<img width="804" height="475" alt="Screenshot 2026-07-16 at 3 29 12 PM" src="https://github.com/user-attachments/assets/7fd7b76a-d873-4412-8d98-697d8c5fc76e" />

*At this point all of your PinOne hardware should have the necessary tools to function properly. I recommend you stop here to reboot your computer and test out the configuration in PinUp Popper/VPX. If if works congratulations! You have a functioning Vpin cabinet! If it does not work take a look at these troubleshooting steps and/or contact the support pages and forums for help! Next steps for DOF configuration are the Addressable LEDs. Remember SSF is a separate system. 

## Addressable LEDS 
### Testing your setup and updating firmware

You can use the config tool to test your outputs and make sure they are all setup OK before trying to get them working in DOF. Download it here: 

[![Get the config tool](../PinOne/Configuring/img/button.svg)](https://github.com/philipellisis/wemos-configurator/releases/latest/download/CSDAddressableControllerTool.exe)


## Configuring Addressable LEDs for DOF

### Prerequisites

Before configuring ALEDs in DOF, you need to have DOF installed. To install and configure DOF, follow the steps mentioned above. After DOF is installed, you can walk through the steps below to configure your ALEDs. The steps below will work if you already have DOF configured for other toys already and they will also work if this is your first time configuring DOF.

### Creating a global config file
1. Creating a GlobalConfig_B2SServer.xml file.
   - In your directoutput folder you will need to access and edit your GlobalConfig_B2SServer.xml. You can make the necessary changes by opening the file in Notepad and then saving once the necessary changes are made.
   - The file location is: C:/DirectOutput/config
   - Right click on GlobalConfig_B2SServer.xml and select “Open with” and then select “Notepad”.
 - This will open the file so that you may make changes.
 - Delete all the current contents of the file.
 - Paste this into the file: 

```xml
<?xml version="1.0" encoding="utf-8"?>
<!--Global configuration for the DirectOutput framework.-->
<!--Saved by DirectOutput Version 3.1.8715.331: 2023-11-23 11-41-48-->
<GlobalConfig>
  <LedWizDefaultMinCommandIntervalMs>10</LedWizDefaultMinCommandIntervalMs>
  <LedControlMinimumEffectDurationMs>60</LedControlMinimumEffectDurationMs>
  <LedControlMinimumRGBEffectDurationMs>120</LedControlMinimumRGBEffectDurationMs>
  <PacLedDefaultMinCommandIntervalMs>10</PacLedDefaultMinCommandIntervalMs>
  <IniFilesPath>C:\DirectOutput\Config</IniFilesPath>
  <CabinetConfigFilePattern>C:\DirectOutput\Config\cabinet.xml</CabinetConfigFilePattern>
  <TableConfigFilePatterns />
  <EnableLogging>true</EnableLogging>
  <ClearLogOnSessionStart>true</ClearLogOnSessionStart>
  <LogFilePattern>.\DirectOutput.log</LogFilePattern>
</GlobalConfig>
```
2. Save the file.

### Relocating your ini files

When DOF is configured without a Cabinet.xml file, you can just put your ini files in the same directory as DOF and it will work fine, if you have a cabinet file you should put all your ini files in the C:/DirectOutput/config directory to ensure they are all read in. This also keeps things a little cleaner now that you will have more than one file for your configuration.

### Creating your cabinet file
In addition to a directoutput.ini file and GlobalConfig_B2SServer.xml file, your addressable LEDs will need a cabinet.xml file.

You will need to create a cabinet.xml file and save it as “cabinet.xml”. Create the new file in this location: C:/DirectOutput/config

- Sample file for this build (you will likely need to adjust the COM PORT to the one your PC uses)

'''
<?xml version="1.0"?>
<Cabinet xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <Name>AddressableLEDSetup</Name>
  <OutputControllers>
    <WemosD1MPStripController>
      <Name>LED Strips 0</Name>
      <NumberOfLedsStrip1>144</NumberOfLedsStrip1>
      <NumberOfLedsStrip2>144</NumberOfLedsStrip2>
      <NumberOfLedsStrip3>256</NumberOfLedsStrip3>
      <NumberOfLedsStrip4>256</NumberOfLedsStrip4>
      <NumberOfLedsStrip5>256</NumberOfLedsStrip5>
      <NumberOfLedsStrip6>256</NumberOfLedsStrip6>
      <NumberOfLedsStrip7>256</NumberOfLedsStrip7>
      <NumberOfLedsStrip8>256</NumberOfLedsStrip8>
      <NumberOfLedsStrip9>256</NumberOfLedsStrip9>
      <NumberOfLedsStrip10>90</NumberOfLedsStrip10>
      <ComPortName>COM1</ComPortName>
      <ComPortTimeOutMs>300</ComPortTimeOutMs>
      <ComPortBaudRate>2000000</ComPortBaudRate>
      <ComPortOpenWaitMs>300</ComPortOpenWaitMs>
      <ComPortHandshakeStartWaitMs>100</ComPortHandshakeStartWaitMs>
      <ComPortHandshakeEndWaitMs>100</ComPortHandshakeEndWaitMs>
      <SendPerLedstripLength>true</SendPerLedstripLength>
      <UseCompression>true</UseCompression>
      <ComPortDtrEnable>true</ComPortDtrEnable>
      <TestOnConnect>true</TestOnConnect>
    </WemosD1MPStripController>
  </OutputControllers>
  <Toys>
    <LedStrip>
      <Name>Right Side</Name>
      <Width>1</Width>
      <Height>144</Height>
      <LedStripArrangement>LeftRightBottomUp</LedStripArrangement>
      <ColorOrder>RGB</ColorOrder>
      <FirstLedNumber>1</FirstLedNumber>
      <FadingCurveName>SwissLizardsLedCurve</FadingCurveName>
      <Brightness>100</Brightness>
      <OutputControllerName>LED Strips 0</OutputControllerName>
    </LedStrip>
    <LedStrip>
      <Name>Left Side</Name>
      <Width>1</Width>
      <Height>144</Height>
      <LedStripArrangement>RightLeftBottomUp</LedStripArrangement>
      <ColorOrder>RGB</ColorOrder>
      <FirstLedNumber>145</FirstLedNumber>
      <FadingCurveName>SwissLizardsLedCurve</FadingCurveName>
      <Brightness>100</Brightness>
      <OutputControllerName>LED Strips 0</OutputControllerName>
    </LedStrip>
    <LedStrip>
      <Name>Back Panel</Name>
      <Width>112</Width>
      <Height>16</Height>
      <LedStripArrangement>TopDownAlternateRightLeft</LedStripArrangement>
      <ColorOrder>RGB</ColorOrder>
      <FirstLedNumber>289</FirstLedNumber>
      <FadingCurveName>SwissLizardsLedCurve</FadingCurveName>
      <Brightness>100</Brightness>
      <OutputControllerName>LED Strips 0</OutputControllerName>
    </LedStrip>
    <LedStrip>
      <Name>speaker leds</Name>
      <Width>1</Width>
      <Height>90</Height>
      <LedStripArrangement>RightLeftBottomUp</LedStripArrangement>
      <ColorOrder>RGB</ColorOrder>
      <FirstLedNumber>2081</FirstLedNumber>
      <FadingCurveName>SwissLizardsLedCurve</FadingCurveName>
      <Brightness>100</Brightness>
      <OutputControllerName>LED Strips 0</OutputControllerName>
    </LedStrip>
    <LedWizEquivalent>
      <Name>LedWizEquivalent 30</Name>
      <LedWizNumber>30</LedWizNumber>
      <Outputs>
        <LedWizEquivalentOutput>
          <OutputName>Right Side</OutputName>
          <LedWizEquivalentOutputNumber>1</LedWizEquivalentOutputNumber>
        </LedWizEquivalentOutput>
        <LedWizEquivalentOutput>
          <OutputName>Left Side</OutputName>
          <LedWizEquivalentOutputNumber>4</LedWizEquivalentOutputNumber>
        </LedWizEquivalentOutput>
        <LedWizEquivalentOutput>
          <OutputName>Back Panel</OutputName>
          <LedWizEquivalentOutputNumber>7</LedWizEquivalentOutputNumber>
        </LedWizEquivalentOutput>
        <LedWizEquivalentOutput>
          <OutputName>Back Panel</OutputName>
          <LedWizEquivalentOutputNumber>10</LedWizEquivalentOutputNumber>
        </LedWizEquivalentOutput>
        <LedWizEquivalentOutput>
          <OutputName>Back Panel</OutputName>
          <LedWizEquivalentOutputNumber>13</LedWizEquivalentOutputNumber>
        </LedWizEquivalentOutput>
        <LedWizEquivalentOutput>
          <OutputName>Back Panel</OutputName>
          <LedWizEquivalentOutputNumber>16</LedWizEquivalentOutputNumber>
        </LedWizEquivalentOutput>
        <LedWizEquivalentOutput>
          <OutputName>Back Panel</OutputName>
          <LedWizEquivalentOutputNumber>19</LedWizEquivalentOutputNumber>
        </LedWizEquivalentOutput>
        <LedWizEquivalentOutput>
          <OutputName>Back Panel</OutputName>
          <LedWizEquivalentOutputNumber>22</LedWizEquivalentOutputNumber>
        </LedWizEquivalentOutput>
        <LedWizEquivalentOutput>
          <OutputName>Back Panel</OutputName>
          <LedWizEquivalentOutputNumber>25</LedWizEquivalentOutputNumber>
        </LedWizEquivalentOutput>
        <LedWizEquivalentOutput>
          <OutputName>speaker leds</OutputName>
          <LedWizEquivalentOutputNumber>28</LedWizEquivalentOutputNumber>
        </LedWizEquivalentOutput>
      </Outputs>
    </LedWizEquivalent>
  </Toys>
</Cabinet>
'''

  - Copy this text in the cabinet.xml file and save.
- For differing setups:
  - The cabinet file for Addressable LEDs is a little complicated to build, so I have created a simple online helper to generate it for you. Simply enter your specific needs and it will be created. Copy the text from the code created below and save it as `cabinet.xml` inside your `C:/DirectOutput/config` directory.


You can find the cabinet file generator [Here](./cabinetGenerator)

### Final Steps

At this point your `C:/DirectOutput/config` directory should look like the following below:

<img width="804" height="475" alt="Screenshot 2026-07-16 at 3 29 12 PM" src="https://github.com/user-attachments/assets/7fd7b76a-d873-4412-8d98-697d8c5fc76e" />

