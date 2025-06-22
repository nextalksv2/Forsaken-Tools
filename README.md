# A short documentation for maps in Forsaken Tools

You can find help with any questions or problems in the official [discord server](https://youtu.be/xvFZjo5PgG0?list=RDxvFZjo5PgG0)

## Basic configuration

Each map has should be a folder, which contains the map including its events and other stuff. In the folder there should be 3 attributes, ``MapName, MapCreators, RenderImage, AmbienceID, CanJump``
![alt text](https://github.com/nextalksv2/Forsaken-Tools/blob/main/MiscAssets/NewMapOptions.png?raw=true)

## Adding map creators/contributors

Adding map creators/contributors is really easy, all you have to do is type a players username or userid, and to add multiple creators you can separate them by a comma like this (with no spaces of course)
![alt text](https://github.com/nextalksv2/Forsaken-Tools/blob/main/MiscAssets/MapCreators.png?raw=true)

## What is ``CanJump``

``CanJump`` is a attribute that when set to true players will be able to jump on the map. Just so that some people dont think that this attribute means that the **map** can jump.

## Adding map ambience

In the ``AmbienceID`` attribute you can put any sound id you want, but make sure that the sound id public and can be used be other users. Or you could use a forsaken ambience
- Yorick's resting place ``134816263052711``
- Pirate bay ``115429958347275``
- Horror hotel ``94877649807774``
- Glass houses ``116648874354780``
- Brandon works ``83891000744628``
- Planet voss ``82047489758400``  

alternatively you could just leave the ``AmbienceID`` blank and the game will use the default ambience

## Adding a map render image/thumbnail

To add a thumbnail for a map all you have to do is.
- First is to create an actual render of your map, which is really easy and can be done in roblox studio.
1. Go to the `TEST` tab and turn on `Device` and then set the resolution to `HD 1080 1920x1080` it should look like this
![alt text](https://github.com/nextalksv2/Forsaken-Tools/blob/main/MiscAssets/MapRenderStep1.png?raw=true)
2. Next find a good spot for a thumbnail
3. Change the type of the resolution to `Physical Size`
4. Take a screenshot, inside the `VIEW` tab
- Next step is to upload the thumbnail to roblox
1. Your screenshot can be found in `C:\Users\youruser\Pictures\Roblox`
2. Upload your thumbnail to roblox.
3. Copy the asset id.
4. Paste the asset id into the `RenderImage` attribute.

## Adding and editing events

## Adding events
To add a event you must first know what type of event you want to add, currently there are 3 events that can be added `OnKillerTouched, OnSurvivorTouched, OnActorTouched` (This does not mean that there can only be 3 events in one map, you can add more events by naming them differently or not, it really doesn't matter). Here is a simple explanation of how every event works and how to use it.

And just before we start. `ToTouchInstance` is a `ObjectValue` inside the event that is used for some events and its only purpose is to tell the `EventsHandler` script which event should be triggered. A `ToTouchInstance` should look like this.
![alt text](https://github.com/nextalksv2/Forsaken-Tools/blob/main/MiscAssets/ToTouchInstance.png?raw=true)

## Events

- OnKillerTouched  
This event requires a `ToTouchInstance` inside with a value of what part the event should be triggered after touching and this event only triggers when a Killer steps on a part.
- OnSurvivorTouched  
This event requires a `ToTouchInstance` inside with a value of what part the event should be triggered after touching and this event only triggers when a Survivor steps on a part.
- OnActorTouched  
This event requires a `ToTouchInstance` inside with a value of what part the event should be triggered after touching and this event only triggers when a player (Survivor or Killer) steps on a part.

## Adding and editing functions

Functions are the actual stuff that happens when a event is triggered. As of right now there are sadly only 2 functions because there really in my opinion aren't any more functions needed to make a map. Anyways before i show the 2 functions i want to explain how a function works and how to use it, for example. This is a stun event (thats what i called it, its not a real event its just a display name). As you can see there is a function inside called ApplyStatus which is a ObjectValue and inside that function there are 4 attributes `Duration, Hidden, Level, Status` this function well applies a status to the actor (player) that steps on the stun part
![alt text](https://github.com/nextalksv2/Forsaken-Tools/blob/main/MiscAssets/StunExample.png?raw=true)

### Something to note is that there can be multiple functions in one event.

## Functions

- ApplyStatus  
This function is quite straight forward its a `ObjectValue` that requires only 3 attributes `Status` being the status name, `Duration` being the duration for which the player will have the status for (in seconds) and `Level` being the status level. Optionally you can also add another attribute `Hidden` which basically hides the status effect from the player.
- KillActor  
Kills the actor (player), duh

## Whitelisting a map

To whitelist a map, all you have to do is

- Before you publish / whitelist a map first check if your map looks something like this ``Buttons`` and ``Misc`` folders are not important and can be deleted unless you have some important stuff inside like map parts and parts that are tied to events.  

![alt text](https://github.com/nextalksv2/Forsaken-Tools/blob/main/MiscAssets/BeforeExport.png?raw=true)
- Publish your map to roblox, **DO NOT** publish the model called **Map** publish the folder with your map name.
- **Make sure that your map that you've published is set to public or else the map will NOT be added, you can make a map public by setting Distribute on Creator Store to true in the maps configuration on the roblox website**
- Join your Forsaken Tools private server or create a private server if you don't have one already
- Open the command panel and click on the ``Whitelist`` button, it will take a while but you will be teleported to another game in which you will be able to whitelist your map.
