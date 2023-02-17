## ExportUtilityWwise 

## What is it?
A C# console application for exporting audio from Unreal Engine games that use Wwise, and converting them into wave (WAV) format.

You input a Wwise event name and extract the .wav file corresponding to the event.

## Requirements
This project requires the following software:

.NET Framework 6 or later
VgmStream, which can be downloaded from https://github.com/vgmstream/vgmstream/releases/latest/download/vgmstream-win.zip
## Usage
1. **[Download latest](https://github.com/djhaled/ExportUtilityWwise/releases)**
2. Extract .zip file to a folder
3. Edit the AudioExportConfig.json file to set the game directory, AES key, object path, export directory, and game override.
   ```js
   gameDirectory    = "Path to Game PAK files."
                    // .."C:\\Riot Games\\VALORANT\\live\\ShooterGame\\Content\\Paks"
   aesKey      = "Game encryption key (if any)"
                    // ..0x4BE71AF2459CF83899EC9DC2CB60E22AC4B3047E0211034BBABE9D174C069DD6
   objectPath  = "Path to the audio event you want to download"
                    // .."ShooterGame/Content/WwiseAudio/Events/SFX/UI/Events_UI_InGame/InGame Play_sfx_UI_MatchVictory.uasset"
   exportDirectory = "Path to your export folder "
                   // ..D:\\AudioExportsGame
   gameOverride = "IMPORTANT: the unreal version your game is in"
                  // ..GAME_Valorant / GAME_SeaOfThieves

   ```
4. Run the ExportUtilityWwise.exe file.
5. Check for MediaExports folder to see all your audio exports and their names

## Support
discord: bK#6198 

## License
This project is licensed under the MIT License. See the LICENSE file for details.
