# vTuber-Virtual-Production-Studio-Assets

![](https://i.imgur.com/2kgB34a.jpg)
(Legacy Asset Pack, Please see updates)

## Summery
This is a Unity Project file for doing virtual productions in VRChat. It features a system with 9 cameras, and 12 overlay slides. You can apply these assets and workflows to your worlds to capture multi-camera realtime footage from within vrchat, podcasts, and music videos. This package would be a good starting point for anyone interested in a do-it-yourself approach to making virtual productions. The picture is the "legacy version" and the updated version is posted below. If you have any questions please let me know!


I am working on this by myself with help from my friends, currently just moved, but I plan on updating this package as time goes on with this work evolving it into Web3 stacks. If you would like to support this project please donate to http://streamlabs.com/boomboxheads to help cover development costs, if you are into crypto my ETH addy is 0x670A6EB62f5146d4B3B40C7b58AA31d175E3d6Fb much love!


## Downloads and Dependencies
-This was built on Unity **2018.4.20f1** (with VRChat in mind)
-The cameras use some "movement" scritps from the **Standarad Assets** that was on the Unity Asset Store.
(https://assetstore.unity.com/packages/essentials/asset-packs/standard-assets-for-unity-2017-3-32351)
-**VRChat SDK** will be needed to use the Template packages (for Multiplayer VR Builds)
These studios work in VRChat and include a modified version of the "Hangout Player" that can be found at VRCPrefabs Forum. 

**UPDATED VERSION**: vTuber Cameras Podcast Shell SDK2 VRChat Unity Project 2018.20f1 https://drive.google.com/file/d/1Z_LpFNJ2HOvwn2v_7CFaShjw-OWHRc0T/view?usp=sharing
This version is the most updated version. If you have any questions please just reach out and ask me. Cheers!![](https://i.imgur.com/r1Ua9Ad.jpg)
Test the world here: https://vrchat.com/home/launch?worldId=wrld_9d9f2bbc-20b2-4826-86d2-689e200a14fd&instanceId=0


## Instructions (Keyboard Controls for PC User)
* 1-9 keys will swap between cameras
* Minus Key (-) goes to Overlay mode to display 

Slides (Use Numeric Keypad)
* 0-9, (.), (+) to change slides

* F - Map Cam To Screen
* L - Camera Light
* G - Greenscreen
* M - Animate TV Down
* / - Zoom


## Camera Controls
When the keyboard controls are pressed (1-9) the camera seleted will be Set to Active, while the others are set to Inactive. This will feed the main camera output(render texture) The camera previews can be seen on the camera preview panel using Render textures as well( at a lower resolution for optimization. ) The camera previews are a duplicate of the main camera with all of the exact same parameters, except they feed a render texture so that you can preview the cameras before switching.

## General Workflow
To make a custom production, we create and customize a set, configure the locations of the cameras, animate the cameras, then during runtime, we use the camera control panel to switch between these cameras with a camera operator in real time. We have a version of this studio running inside VRChat, and use that software as our networked IK, motion capture, and avatar layer. We are capturing the video output with OBS (Open Broadcast Software) from the game engine we are rendering our scene in. 

Depending on the platform you are planning to work on. The approach will be different. Currently we use platforms like VRChat (Unity3d), and Unreal Engine to do virtual productions over the network.

It is common to use many platforms to create a virtual production.

## Slides / Overlay
This system was designed with presentations in mind so we have an extra camera that renders planes in front of a camera to create the illusion of an Overlay by pushing (-) Minus Key. It is sort of a work around, and if you would like to extend or make this package better or more optimised, please feel free to submit a request. Thanks!

We swap out 12 different Slides(show/hide gameObjects) using the numeric keypad. 

You can swap out the pictures of the slides before building the production by changing the textures in the SLIDES folder, by editing the materials. We import jpegs, and add them to the respective materials before we do the production. A possible extention to this would be to use a URLLoader to have dynamic materials and slides. 

## Arranging The Cameras
Move the cameras (via the Parent Object) and feel free to animate or extend the cameras to do even more things like add more scripts and functionality as needed. If the camera are designed to be moved as rigid body, make sure to put the rigid body, and pickup scripts on the parent object to maintain the camera heirchy. Arrange the cameras around your set by translating the cameras manually, and checking the camera preview object to see how it looks in frame.

## Pro-Tip: 
Because of the way the camera previews work, you should only move the Master Root of each camera. You can add an additional Parent object to the cameras if you like, and animate those for animated camera tracks. The switches use SetGameObjetActive to turn on and off the cameras. I diddnt use an array, and instead just use conditions and input to swap cams, because of uSharp (VRC SDK constraints) and kept the code as simple as possible. The code can be re-written, and of course extended to do many more things then just switch cameras. i.e. Zoom camera shake, change post porocessing lens.

## Camera Culling / Hiding Objects From Cameras
If you would like to hide / show things in the camera output, you would setup layers and use camera culling with a "SeenByCamera" layer and "GreenScreen" culling layers for teh reflection probe not to reflect the greenscreens.


## Do you need a Custom Studio?
Our crew is available for comission to create CUSTOM VR Production studios for podcasts, music videos, films, concerts, events, and other productions. We will curate models based on the budget and deisgn, light, and customize your production studio to meet your needs. If you have any custom productions in mind, please feel free to reach out! @godfreymeyer

## Examples
Please check out the examples and tutorials on my youtube page to get familiar on the workflow on virtual prodcutions. These asset can be ported to work in any game engine, and the basic camera control scipts have been written in C# and would have to be ported to work on other platforms tah Unity. Using platforms like VRChat, we have filmed many music videos, podcasts and events in VR using this system as a base. It has sped up production when making rooms or builds for vTubing, vPodcasts, and vFilms, and endless "over the network, real-time collaborative" projects. 

## Legacy Versions Of This Camera System
There are different versions of this suite. If you had built a studio on the older version. Here is a link to that project, but I suggest you update to the new system, I will not be supporting the Legacy System anymore unfortunatly. 
*Legacy* VRC SDK2 Complete Project (With All Assets) https://drive.google.com/file/d/15jAm3EPSTKnkhMjjMzsJxeEzn09iHol_/view?usp=sharing
Test Legacy World Here: https://vrchat.com/home/launch?worldId=wrld_9842d4fc-0c40-4e00-887e-5f2ef596c65c&instanceId=0

## Web Resources:
http://Unity3d.com/
http://vrchat.com/
https://assetstore.unity.com/packages/essentials/asset-packs/standard-assets-for-unity-2017-3-32351

Special thanks to Jin, the VR Devs, and the Web XR community for helping in various way to make this possible.

Please subscribe to my youtube page http://www.youtube.com/godfreymeyer and check out more on my guthub github.com/gm3 Much love!


## Contact

Please check out some our productions on [Youtube](https://www.youtube.com/results?search_query=godfrey+meyer&page=&utm_source=opensearch) "Godfrey Meyer" or [#boomboxhead](https://www.youtube.com/results?search_query=%23boomboxhead) to find videos. If you have any questions please feel free to reach out to me #boomboxhead on discord `boomboxhead#5796`. @godfreymeyer on twitter. Have fun and link me to the videos you make, thanks!
