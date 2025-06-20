# A short documentation for maps in Forsaken Tools

You can find help with any questions or problems in the official [discord server](https://youtu.be/xvFZjo5PgG0?list=RDxvFZjo5PgG0)

## Basic configuration

Each map has should have be a folder, which contains the map including its events and other stuff. In the folder there should be 3 attributes, ``MapName, MapCreators, RenderImage``
![alt text](https://github.com/nextalksv2/Forsaken-Tools/blob/main/MiscAssets/MapAttributes.png?raw=true)

## Adding map creators/contributors

Adding map creators/contributors is really easy, all you have to do is type a players username or userid, and to add multiple creators you can separate them by a comma like this (with no spaces of course)
![alt text](https://github.com/nextalksv2/Forsaken-Tools/blob/main/MiscAssets/MapCreators.png?raw=true)

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
To add a event you must first know what type of event you want to add, currently there are 3 events that can be added `OnKillerTouched, OnSurvivorTouched, OnActorTouched`. Here is a simple explanation of how every event works and how to use it.

And just before we start. `ToTouchInstance` is a `ObjectValue` inside the event that is used for some events and its only purpose is to tell the `EventsHandler` script which event should be triggered. A `ToTouchInstance` should look like this.
![alt text](https://github.com/nextalksv2/Forsaken-Tools/blob/main/MiscAssets/ToTouchInstance.png?raw=true)

## Events

- OnKillerTouched  
This event requires a `ToTouchInstance` inside with a value of what part the event should be triggered after touching
