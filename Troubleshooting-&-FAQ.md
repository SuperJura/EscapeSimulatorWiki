# 🤼 Multiplayer

If you have issues with co-op/multiplayer try this:

 - Make sure you are online
 - Make sure you've invited at least one player
 - Try hosting with both normal and legacy hosting mode
 - Disable firewall
 - Make sure all the players have the same game version.
 - Make sure that if you are playing a workshop map, all the players have it installed (just click Subscribe in the Workshop)
 - Try restarting your PC

Steam specific:

 - Make sure you're online and connected to Steam
 - Check if Steam servers are down
 - Verify game files on Steam (right click the game in the Steam library > Properties > Local files > Verify...)

# 🔨 Room Editor

## 📁 Working with folders

<details><summary> <h4>Accessing the custom room UGC folder</h4></summary> 

All custom rooms are located in their own folders in the UGC folder. There is a button in the Room Editor menu that opens the correct room folder for you.
![UGC Button](https://github.com/SuperJura/EscapeSimulatorWiki/blob/main/pictures/RoomEditor/UGCButton.png)

Mac users cannot open it this way because the folder is within the hidden "library" folder that you will need to make visible/accessible.

UGC folder path:
```
Windows: %USERPROFILE%\AppData\LocalLow\Pine Studio\Escape Simulator\UGC
Mac: user/Library/Application Support/Pine Studio/Escape Simulator
```

📓 **Note:** The UGC folder contains your custom created rooms and rooms copied from other creators. Rooms you subscribed to are located in another folder.

</details>

<details><summary><h4>How to load a backup of a room</h4></summary> 

1. Open the room UGC folder where the 'Room.room' file is located
2. Rename the 'Room.room' file
3. Open the 'Backups' folder
4. Choose a backup file you want to revert to (probably the one created most recently)
5. Copy and paste the chosen backup file to the place where the 'Room.room' file was
6. Backup files have a different extension, e.g. 'Room.roombk1auto', rename the new backup file to 'Room.room'

Now you can restart the game and load the room in the Room Editor. If the room doesn't appear in the list 'Your Rooms' check the new file extension name again.

⚠️ **Important**: To load the room the file needs to be called exactly 'Room.room'

⚠️ **Important**: Be careful when deleting files, you could lose your room if you delete the wrong files.

</details>

<details><summary><h4>I renamed a file or a folder and the room won't load</h4></summary> 

All folders in the **base UGC** folder need to be named 'Room_*number*'. If you renamed the room folder just rename it back to that format, e.g. 'Room_1' or 'Room_22'.

The **room UGC** folder needs to contain these files:
 - 'Room.room'
 - 'Preview.jpg'
 - 'Id.bin' - if you published the room

If you renamed one of these files rename them back to these names and restart the game.

</details>


<details><summary><h4>My 'Backups' folder is huge, can I delete room backup files?</h4></summary> 

A backup file is created every time you press the play button to test the room while in the Room Editor, which can create a lot of files. You can delete any file from the 'Backups' folder you don't need. 

⚠️ **Important**: Deleting all backup files means you can lose your room if your original 'Room.room' file corrupts.

</details>

<details><summary><h4>What is the 'Id.bin' file?</h4></summary> 

The 'Id.bin' file is created when first publishing the room to the Steam workshop and it contains the ID of the Steam workshop item you published the room to. This file is not uploaded to the Steam workshop when publishing the room and only the publisher of the room should have access to it.

⚠️ **Important**: Deleting this file means you won't be able to update the workshop room.

</details>

## 🎬 Publishing a room

<details><summary> <h4>Room fails to publish</h4></summary> 

1. Make sure you're logged into Steam
2. Make sure Steam servers are up and running
3. Make sure you're on an account that owns the game. Steam blocks uploads to the workshop from accounts that have the game Family shared.
4. Check if there is a 'tempPublish\_Room\_*number*' (e.g. 'tempPublish_Room_3') folder in the folder path below
```
Windows: %USERPROFILE%\AppData\LocalLow\Pine Studio\Escape Simulator\
Mac: user/Library/Application Support/Pine Studio/Escape Simulator/
```
If there is delete it and try uploading the room again.

⚠️ **Important**: Make sure you only delete the folder that starts with 'tempPublish_'.

</details>