# PinOne Mini Machine Quickstart Guide

This is a quick-start guide to test the functionality and set up the PinOne Mini Machine Gaming Controller for PinballFX.

## Pre-requisites
1. Steam is installed and functioning.
2. Pinball FX is installed and functioning.
3. PinOne Mini machine is connected to your PC via USB-C to USB-A cable provided.
4. Power supply is connected to the PinOne Mini Machine and Outlet.

## Quickstart Guide
### Step 1: Enable Generic Controllers in Steam settings.
1. Open Steam.
2. Click the Steam icon in the top left corner and select “settings”.
3. In the Steam Settings menu select “controller” on the left hand side.
4. Select “show advanced settings”.
5. Switch “Enable steam input for generic controllers” on.
<img width="362" height="298" alt="Steam settings" src="https://github.com/user-attachments/assets/390be0a8-33e8-4a7f-9fb0-3f571108734e" />
<img width="840" height="704" alt="Steam controller to advanced settings" src="https://github.com/user-attachments/assets/7732ab4d-785d-48a2-b52b-6211c825ec74" />
<img width="831" height="670" alt="enable steam input for generic controllers" src="https://github.com/user-attachments/assets/b71ac19f-b4db-4edc-9b34-07ca8a770948" />

### Step 2: Download the PinOne Configuration Tool
1. On the Cleveland Software Design Website, navigate to the “Documentation” page located at the top right hand corner of the webpage. 
2. The “Documentation” will take you to a new website dedicated to product specifications, guides, tips, and tutorials. (I highly recommend you read through the entire “PinOne” tab along with all of its subtabs!)
3. Navigate to the PinOne Tab on the left side of the page. 
4. Navigate to the “[PinOne Configuration Tool]([url](https://pinball-docs.clevelandsoftwaredesign.com/docs/PinOne/Configuring/))” subtab.
5. Select “Download”. (Note: this guide is following a windows based set up but Mac and Linux releases for this tool are also linked.)
6. This application may be flagged as an uncommon download. If so make sure to click the arrow and select “keep”.
7. In file explorer, double click the application and select “properties”.
8. From the properties screen select “unblock” and “apply”.
9. Run the application by double-clicking.
<img width="1908" height="1018" alt="Documentation Location" src="https://github.com/user-attachments/assets/a4677980-f899-4e79-aa67-9ef7670bc9ec" />
<img width="1913" height="1023" alt="Start Here Documentation page" src="https://github.com/user-attachments/assets/c65de5f6-7024-4f69-8403-238bcf03b9eb" />
<img width="1919" height="1027" alt="PinOne Configuration tool tab" src="https://github.com/user-attachments/assets/60346542-0874-4e54-9b4f-13a9f5eafab9" />
<img width="1917" height="1023" alt="Config tool download" src="https://github.com/user-attachments/assets/f2d2d1b4-f40e-4acc-b348-4fb148be5c18" />
<img width="1903" height="1021" alt="Keep" src="https://github.com/user-attachments/assets/32ab9286-fc20-4b05-b2f7-3151a16d22a2" />
<img width="1919" height="1031" alt="Properties unblock" src="https://github.com/user-attachments/assets/d00e3f83-e9ef-4232-b05f-2c80487489e9" />

### Step 3: Testing
1. You should be able to press “Connect” and the PC will auto connect to the PinOne. If there is an issue, manually select the COM Port. 
2. After connecting, we will test the controller’s functionality using the tabs on the left-hand side of the screen, accelerometer, inputs, outputs, and plunger.
<img width="1919" height="1020" alt="Pinone config connect" src="https://github.com/user-attachments/assets/59b2dad7-3b42-40ee-8811-790fc1038885" />
<img width="1921" height="1025" alt="Config tool testing" src="https://github.com/user-attachments/assets/60c7e2ba-01ac-4143-a6dc-c77587d23967" />

#### Testing the Accelerometer
Physically move the PinOne Mini Machine and attempt to move the accelerometer across all 4 axis. 

<img width="1919" height="1020" alt="Accelerometer test" src="https://github.com/user-attachments/assets/d1572dea-342c-4efc-8bab-f5ae9572ddd8" />

#### Testing the Inputs
One at a time, press all of the buttons to make sure they are all registering inputs. Buttons 1-9 should be all accounted for.
Note: Buttons 1 and 3 are tied to the solenoids, if you have solenoids in your unit they should activate.

<img width="1919" height="1025" alt="Inputs test" src="https://github.com/user-attachments/assets/e05296aa-b0b6-4f28-a549-0cb8e53b5caa" />

#### Testing the Outputs
The outputs can be tested in two different ways.
First, you can use the slider at the top left of the page by clicking the slider and using the arrow keys to activate the outputs one by one..
Second, under the “Main Outputs” button and “Button Outputs” button there are all of the individual outputs and their settings. You can use the “current value” switch to activate each of the outputs.
Test the outputs.
- Outputs 1 and 2 are the solenoid outputs.
- Outputs 16-31 are the button outputs.
CAUTION:
Do not use the “max value” slider to adjust the output of the solenoids (outputs 1 and 2). Run the solenoids at the full 255, as the Life Extenders and mosfets driving the boards were designed for this use.

<img width="1919" height="1020" alt="Outputs test" src="https://github.com/user-attachments/assets/0f6f52c0-12c3-4472-94da-38a479c80bb1" />

#### Testing and Calibrating the Plunger
1. It is recommended that you calibrate plunger while testing by using the “Run calibration routine”.
2. Follow the steps in the calibration routine.
3. Select “finish calibration”.
4. Select “save config” at the top of the page to apply the settings.

<img width="1919" height="1029" alt="plunger test" src="https://github.com/user-attachments/assets/01dd3015-fe69-40d2-85c6-065f3f93b252" />

#### Settings Tab
If you are using a bluetooth adapter navigate to the settings tabe and switch the “enable bluetooth” switch under “other settings” on. Save the configuration.

<img width="1919" height="1025" alt="Enable bluetooth" src="https://github.com/user-attachments/assets/da9ea407-3c06-4847-8871-ceb583a3f3cf" />

### Step 4: Save the Config
After making any changes to the configuration or calibration, always press the button "save config" to apply these new settings. 

### Step 5: Applying the Steam/Bluetooth Settings.
This step is necessary for using any steam games or using the bluetooth function.
1. Under the “Controller” tab you are able to adjust the button mapping if needed. The buttons are already pre-mapped, so unless alternative mapping is desired, you are good.
2. Select “save steam/bluetooth config”. 
3. This setting will save the controller configuration to the steam files in your PC. It will also apply the configuration to the bluetooth adapter for the Meta Quest 3 if you are using one.
Note: this step must be done after switching “enable generic controllers” in steam settings.
<img width="1919" height="1029" alt="Save bluetooth settings" src="https://github.com/user-attachments/assets/793d3d40-5770-4ca5-aa58-edc446ea500f" />

### Step 6: Disconnect and close the PinOne Configuration Tool and test by launching Pinball FX.
You should have button functionality, solenoids on flipper press, and nudge!


## Common Configuration Changes
Under the “Inputs” tab of the PinOne Configuration Tool there are two common configuration changes people make. So that navigating Pinball FX without a keyboard and mouse is easier and nudge can be tied to button presses in addition to the physical nudge.
1. Shift button
   - In the top left hand corner of the inputs page change the “shift button” from disabled to “button 2”.
   - This will make the right magna save button a shift button so that when holding the right magna save button you activate shift. The reason why you would want this is because while shift is activated, the buttons “A,B,X,Y” on the front of the PinOne Mini Machine become directional and can be used for navigation without a keyboard.
   - Save the Config.
2. Button Press Nudge
   - If you want to have button press nudge in addition to the physical nudge capabilities of the PinOne Mini Machine, then change Input 2’s keyboard mapping to “Right ALT” and Input 4’s mapping to “Left ALT”. This will make your left and right magna saves nudge buttons.
   - Save the config.
<img width="1919" height="1029" alt="Common Configuration changes" src="https://github.com/user-attachments/assets/329e93c9-bbce-4ae0-b4a9-30bc09308ef1" />

## X-Input
X-Input is a downloadable firmware which allows the PinOne Mini Machine to be recognized as an X-input controller. This option is slightly easier set up, but restricts edits to be made to the controller configuration once applied; however, t is reversible. 

Information on the x-input firmware can be found at this link: https://pinball-docs.clevelandsoftwaredesign.com/docs/PinOne/Configuring/#updating-firmware

Information on uninstalling the x-input firmware can be found here: https://pinball-docs.clevelandsoftwaredesign.com/docs/PinOne/Configuring/#installing-firmware-on-boards-with-x-input-installed
(You will need to be running “manual firmware update” while performing this action, because pressing the buttons acts as a reset.)

