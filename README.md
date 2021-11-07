# -abe71-joyGremlin-IL2-BoS-CH-FSPTPPTQCM-VR
Joystick gremlin map for IL2 Sturmovik Battle of Stalingrad

This is a map for one engine aircrafts in IL2-Sturmovik Battle of Stalingrad VR. The Joystick Gremlin map is more or less a augmented 1 to 1 directx map of the the physical controllers to virtual vjoy devices. The difference from a 1 to 1 map is that some axises are moved a little due to some strange bug (on my system?) but fomremost are the 4 modes implemented. And the 2 user plugins used for implementing a temporary mode switch on the pro throttle and a sticky on throttle quadrant.

## Mode controll explained

- Pro thottle temporary mode switch: the two leftmost fingerbuttons controls of the pt controls which of the 4 modes are active, just like a shift button owould do on a keyboard only we have 4 instead of 1 mode.
  - mode 1 release mode buttons
  - mode 2 hold button 4 on the pro throttle (left most "pinky button" on the handle of the trottle)
  - mode 3 hold button 3 on the pro throttle (the button next to button 4 above)
  - mode 4 hold bothe button 3 and 4 on the pro throttle.

- Throttle quadrant stick mode switch
  - next mode: button 1 on the throttle quadrant (left most up). The mode stops cycling at mode 4 it does NOT switch to mode 1 after mode 4.
  - previous mode: button 2 on the throttle quadrant (left most down). The mode stops cycling once mode 1 is reached.
  - If any of the mode buttons on the pro throttle is used that mode takes over and when the pro throttle buttons are the release the mode is resetted to 1.

## Installing necessary software
- vjoy
  - The ch controllers are remapped via vjoy. Installation instructions are here: https://sourceforge.net/projects/vjoystick/
- Joystick Gremlin
  - This controller are programmed with Joystick Gremlin. To install it follow the instructions on this page: https://whitemagic.github.io/JoystickGremlin/
- HidHide
  - IL2 can only handle up to 8 controllers and we will be using 6 of these. Therefore we need to hide the controllers we will not use. This is done through HidHide. Installation instructions here: https://github.com/ViGEm/HidHide

## User guide
### Vjoy
1. After installing all the necessary software (see above) vjoy needs to be configured. Launch the configure vjoy app. Now make sure you have 6 devices, device 1 to 6. Mark the device you want to add in the tabs on top and push the add device button for each of the 6 devices.
2. Now click on tabs and make sure it has no forece feedback and exactly the axises, nr buttons and nr POVs as om the table below:
- vjoy1	Axises: x,y,z 		 Buttons: 32 	 POVs 2
- vjoy2	Axises: x,y			Buttons: 32		POVs 2
- vjoy3	Axises: x,y,z,Rx,Ry,Rz	Buttons: 24		POVs 0
- vjoy4	Axises: x,y,z,Rx		 Buttons: 32 	 POVs 0
- vjoy5	Axises: none			 Buttons: 32 	 POVs 2
- vjoy6	Axises: none			 Buttons: 24 	 POVs 0

The reason for having this many virtual controllers is that IL2 can not handle controllers with more than 32 buttons, POVs not counted.

### Joystick Gremlin
- After adding the vjoy devices start Joystick Gremlin. 
- Then File/Load Profile. Select il2JoyGremlin.xml from this repository.
- Now you probably will need to readd the user plugins. Got to the plugin tab and add plugin at the bottom. Add both *.py files from this repository.
- Activate the map by pressing the controller icon below the menu line

### HidHide
IL2 can handle at most 8 controllers in total. Since this map is using up 6 of these with its virtual controllers based upon 4 physical controllers this already is 10 controllers on the system. It is therefore essential to hide the controllers not in the map for IL2. This is done via a nice tool called HidHide.

To hide all game controllers not in the map from the system. To do this start hidHide.
- Add Joystick Gremlin to the Applications tab, it will allow Joystick Gremlin to keep seeing the physical controllers it needs.
  * Default path is C:\Program Files (x86)\H2ik\Joystick Gremlin\joystick_gremlin.exe
- Go to the Devices tab and tick all gontrollers not in your map.
- Remember to also tick Enable device hiding at the bottom
- To verify the result press Win - R and type: joy.cpl. You should see only your 6 virtual devices. From here you can also verify the function of your map.

### IL-2 configuration
- Make a backup of ...\IL-2 Sturmovik Battle of Stalingrad\data\input\
- Remove the file devices.txt (if any) from ...\IL-2 Sturmovik Battle of Stalingrad\data\input\
- Copy all current.* from the repository to ...\IL-2 Sturmovik Battle of Stalingrad\data\input\
- Start IL2 and close it as soon as it has started
- Open ...\IL-2 Sturmovik Battle of Stalingrad\data\input\devices.txt
- Reorder the devices in the devices.txt so that the
  * vJoy1 device is at 2:nd line (immideately after the header configId,guid,model|) at 1st position.
    - Set configId to 0 for it
    - add | at end of the line if necessary.
  * vJoy 2 at second position
    - set configId to 1
    - and add | if necessary
  * repeat for all controllers adding them in the order specified in vJoy, setting config id one higher for each.
  * Rmeove the | on the last line if any.
  * See exampleDevices.txt in the repository
- Start IL-2 again and try out your new controller map.

### Contribute to this repository
- Configure your own map and create a branch with it on git hub to share it with others! 
- Be sure to make a pull request to the develop branch with it when you are happy with it. Remember to add your IL2 configs before making the PR!
	
  