# -abe71-IL2-BoS-CH-FSPTPPTQCM-
CH - products map for IL2 Sturmovik Battle of Stalingrad


This is a repository for one engine aircrafts in IL2-Sturmovik Battle of Stalingrad VR. The CH map makes use of IL2s default settings where ever possible.

The map is based on my old profile for IL2-Forgotten Battles and is still in the early stages of configuration so there are "dead" commands in the .CMC and some buttons still have the FB commands mapped. The most important functions works though, so this map can be used and refined for BOS.


I make use of "non sticky modes", the two leftmost fingerbuttons controls which of the 4 modes are active, just like the shift button would do. This is extra great when playing in VR since it is impossible to see the mode indicator on the joysticks.


# IL-2 configuration
	*  Make sure to download your map in the CH control manager and then start IL-2.
	*  Startup IL-2 and  exit it again
	*  Make a backup of ...\IL-2 Sturmovik Battle of Stalingrad\data\input\
	*  Copy all current.* from the repository to ...\IL-2 Sturmovik Battle of Stalingrad\data\input\
	*  Rearrange the controllers in the devices.txt so the CH - virtual controllers comes first, from zero to 3.
	*  Start IL-2 again and try out your new controller map.
	*  Configure the map to your taste and create a new branch on git hub to share it with others! 
	*  Be sure to make a pull request to the develop branch with it when you are happy with it. Remember to add your IL2 configs before making the PR!
	

# Rearranging the controllers

Make sure the CH%20Control%20Manager%20Device%201 - CH%20Control%20Manager%20Device%201 in order, remember to change the configId (leave the rest):
  - Note that the lines should end with a '|', except for the very last controller in the entire list. The list might have more entries than in the example below.

Example (the guid is probably different for you)
configId,guid,model|

0,%2227fa00a0-a5c7-11e7-0000545345440280%22,CH%20Control%20Manager%20Device%201|

1,%2227fa00a0-a5c7-11e7-0000545345440480%22,CH%20Control%20Manager%20Device%202|

2,%2227fa00a0-a5c7-11e7-0000545345440180%22,CH%20Control%20Manager%20Device%203|

3,%2227fa00a0-a5c7-11e7-0000545345440380%22,CH%20Control%20Manager%20Device%204


# Running the control manager
The ch controlers do not support power saving or fast startup. The CH Control manager is no loginger maintained and needs to be run in as administrator in compatability mode for Win Vista SP2 to work.

	* Deactivate windows fast startup
		- https://winbuzzer.com/2020/05/19/how-to-disable-windows-10-fast-startup-hiberboot-hybrid-boot-hybrid-shutdown-xcxwbt/
	* Disable USB power saving
		- https://www.techwalla.com/articles/how-to-turn-off-a-usb-ports-power-save-option
		- https://answers.microsoft.com/en-us/windows/forum/windows_10-other_settings/usb-settings-in-power-plan-options-on-windows-10/38753b89-65d0-49c1-8f91-2bb50f9b19a0

Also there seems to be an issue that the CH maps gets only partially downloaded. At least on my slow old rig	I have to repeat the download 5-6 times before all mappings are registered.
  - Use the key check utility in the control manager to check that every button is working.
  