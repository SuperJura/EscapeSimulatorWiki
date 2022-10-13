When reporting a bug, remember to:
- First check the [troubleshooting page](https://github.com/SuperJura/EscapeSimulatorWiki/wiki/Troubleshooting-&-FAQ)
- Explain what the issue is and what happened immediately before
- Add the '*Player.log*' file to the bug report
- If possible add a screenshot that shows the issue
- If possible write down step by step instructions on how to reproduce the bug

'*Player.log*' file location:
```
Windows: %USERPROFILE%\AppData\LocalLow\Pine Studio\Escape Simulator\Player.log
MacOS: ~/Library/Logs/Pine Studio/Escape Simulator/Player.log 
Linux: ~/.config/unity3d/Pine Studio/Escape Simulator/Player.log
```

⚠️**Important:** The '*Player.log*' file is overwritten each time the game is started, so it is important to upload it as soon as the bug happens without restarting the game.

## 🤼 Multiplayer
If you're playing a multiplayer game and you run into some issues there are a couple more files you need to add to the bug report:

 - '_GameVersion_\__LobbyID_\_Host.packets' and '_GameVersion_\__LobbyID_\_Client.packets'
 - 'Net.log'

From the files, we can see what happened in both games and can recreate bugs. If you can’t upload the files due to size, compress them using '.zip' or something similar.

<details><summary> <h4> 📄 '.packets' files</h4> </summary>

You need to upload **BOTH** '*.packets*' files for Host and Client on the channel. The files are stored after you end a multiplayer game and they need to have the same *GameVersion* and *LobbyID*. 
The '.packets' files are stored in:
```
Windows: %USERPROFILE%\AppData\LocalLow\Pine Studio\Escape Simulator\Multiplayer
MacOS: ~/Library/Logs/Pine Studio/Escape Simulator/Multiplayer
Linux: ~/.config/unity3d/Pine Studio/Escape Simulator/Multiplayer
```
⚠️**Important:** The files **WILL NOT** be on the same computer. One will be on the computer of the host, one will be on the computer of the client(s).

For example, if two players finish a room with *LobbyID* 'DD520' on *GameVersion* '11699', there will be two '.packets' files you need to add to the bug report:
 - '11699_DD520_Client.packets' from the client computer
 - '11699_DD520_Host.packets' from the host computer

</details>
<details><summary> <h4> 📄 'Net.log' file</h4> </summary>

The 'Net.log' file is stored in:
```
Windows: %USERPROFILE%\AppData\LocalLow\Pine Studio\Escape Simulator\Net.log
MacOS: ~/Library/Logs/Pine Studio/Escape Simulator/Net.log
Linux: ~/.config/unity3d/Pine Studio/Escape Simulator/Net.log
```
⚠️**Important:** The '*Net.log*' file is overwritten each time the game is started, so it is important to upload it as soon as the bug happens without restarting the game.

</details>

