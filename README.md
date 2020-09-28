# CnC_Remastered_Collection - Danku's Mod

A WiP mod for the Command &* Conquer Remastered Collection - Tiberian Dawn.

* Original Source Code - https://github.com/electronicarts/CnC_Remastered_Collection
* Refactored Source Code for modern VS Code - https://github.com/alexlk42/CnC_Remastered_Collection

## Running Locally

### Development Setup / Creating a Build
* Load .sln into VS Code 2019
* Define `WINDOWS_IGNORE_PACKING_MISMATCH`:
  * Open TiberianDawn Property Pages
  * C/C++ -> Preprocessor
  * Add to Preprocessor Definitions
* Build

## Integrating Mod with Game Client

1. Create directory with name for mod - this should go in `~/Documents/CnCRemastered/Mods/Tiberian_Dawn`
2. Inside your new mod directory create json file called ccmod.json - See below sample

```json
{ "name": "Your Mod Name", "description": "Description of your Mod", "author": "Danku", "load_order": 1, "version_low": 2, "version_high": 1, "game_type": "TD" }
```
3. Create new directory alongside ccmod.json inside your mod directory called Data
4. Put TiberianDawn.dll in this new Data directory
5. Launch game client and you should be able to load the mod under options -> mods. Check this option and wait for the client to restart with your updated mod in place.

Note: Multiplayer settings are disabled when running a mod in the game client. In order to play with colleagues on a modded client you will need to use a hosted VPN service like Hamachi
