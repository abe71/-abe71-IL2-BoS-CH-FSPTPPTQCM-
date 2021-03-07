# -abe71-IL2-BoS-CH-FSPTPPTQCM-
CH - products map for IL2 Sturmovik Battle of Stalingrad


This is a repository for one engine aircrafts in IL2-Sturmovik Battle of Stalingrad VR. The CH map makes use of IL2s default settings where ever possible.

The map is based on my old profile for IL2-Forgotten Battles and is still in the early stages of configuration so there are "dead" commands in the .CMC and not all buttons are correctly mapped. The most important functions works though.


In this map I make use of "non sticky modes", the two leftmost fingerbuttons controls which of the 4 modes are active, just like the shift button would do. This is extra great when playing in VR since it is impossible to see the mode indicator on the joysticks.


# IL-2 configuration
	*  Make sure to download your map in the CH control manager and then start IL-2. 
	*  Open a explorer window to ...\IL-2 Sturmovik Battle of Stalingrad\data\input\
	*  Rename the current.map to current.map.bak
	*  Copy the current.map from this repo to the input folder of IL-2
	*  Startup IL-2 and  exit it immidiately
	*  Rearrange the controllers in the devices.txt so the CH - virtual controllers comes first, from zero to 3.
	*  Start IL-2 and try your new controller map.
	*  Configure the map to your taste and create a new branch on git hub to share it with others! 
	*  Be sure to make a pull request to the develop branch with it when you are hapy with it!
	

# Rearranging the controllers

Make sure the CH%20Control%20Manager%20Device%201 - CH%20Control%20Manager%20Device%201 in order, remember to change the configId (leave the rest):

Example (the guid might be different for you)
configId,guid,model|

0,%2227fa00a0-a5c7-11e7-0000545345440280%22,CH%20Control%20Manager%20Device%201|

1,%2227fa00a0-a5c7-11e7-0000545345440480%22,CH%20Control%20Manager%20Device%202|

2,%2227fa00a0-a5c7-11e7-0000545345440180%22,CH%20Control%20Manager%20Device%203|

3,%2227fa00a0-a5c7-11e7-0000545345440380%22,CH%20Control%20Manager%20Device%204|
