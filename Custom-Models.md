# Supported model formats
* .gltf
* .glb

# Custom Models intro
Because the model path is used as the prop ID a model can be replaced by replacing it with a model with the same name and in the same folder or by renaming all of its instances in the Room.room file and then reloading the room.
Models can be loaded while in the Room editor, just place the model in the "_CustomModels" folder and open the Custom category in the editor to check for changes in the files.
Animated models are created as Skinned Mesh Renderers.

# Custom Models Colliders
When standard (non modified) models are imported they get a box collider that encompasses all of the visible parts of the model (except for the Skinned Mesh Renderers, which have some problems with that type of collider generation). Those models with a generated box collider will have a check mark so you can choose if you want to use it in the game without using the Visibility Activator to disable it. This way you can easily parent the new Collider Components to the imported model and create your own colliders. When using the Visibility Activator Component for disabling Collider components you will need to disable each Collider component individually or parent them to an Empty and disable the Empty object.
If you want even more performance it is recommended to modify the model and add colliders that way instead of adding the Collider Component children. When loading a model we check each mesh name and if the mesh name ends with "#boxcollider" we add a box collider (everything after the first "." in the name is ignored so "meshname#boxcollider.001" is still a valid collider name). In order to add a collider to the model you just need to add as many cube meshes as needed and size and rotate them to encompass most of the model. Most of the original prop colliders are created similarly using box colliders as children of the main rendering part. When the colliders have been added this way, the check mark for disabling the collider is removed, but you can use the Visibility Activator Component on it as usual.

# Deleting a model from the "_CustomModels" folder
If the model was deleted while not in the editor and the files were not used in the room nothing will happen. It just won't be loaded when you go to edit the room.
If the model was deleted while in the editor you will still be able to place the model in the room and use it, but it is recommended to remove all instances present in the room and save.
If a model was deleted and it was used in the room, when loading the room you will get a room loading error which states that custom models have been deleted. You can check the "player.log" file and find exactly which files are considered missing and replace them or go into the room and delete all of the default props that were loaded instead of the custom model. If a room with missing custom models is uploaded players will not be able to start it. Even if you save the room with the loaded default props they are still considered missing props.

# Tips
If possible modify the model to only contain one mesh object. Multiple mesh objects result in multiple gameobjects.
When publishing a room only the used models are uploaded to the workshop.



