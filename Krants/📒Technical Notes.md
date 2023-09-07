- To fix PC Players GUI not working in presence of VR Player, make VR Player UI pointer disabled by default and enabled if is owner of client
    - If this doesn't work try creating a prefab of the VR Players UI pointer and delete it from the VR Player prefab, then if photon view says this client is the owner of the VR Player, instantiate the UI pointer as usual but only locally

- VR Player head collision events should be owned by the VR Player's photon view
    - In general, localize all events onto the player being affected rather than the player causing the event


- To add VR Player hand offsetting, go to VR Player > TrackerOffsets > Contoller ([right/left]) and edit the transform
    - Be sure to save the players preferances in playerdata so that the player doesnt need to change their offsets on each start


- Save PC Player settings in palyerdata so that the player doesn't need to change to their preferred settings each time they load