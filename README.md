# Dungeon Siege 1 Troubleshooting Guide

## Table of Contents
   
* [1.0 Glossary](#glossary)
* [2.0 Guides](#guides)
   * [2.1 Add the game on GameRanger](#add-the-game-on-gameranger)
   * [2.2 Capture the game with OBS](#capture-the-game-with-obs)
   * [2.3 Change the FOV](#change-the-fov)
   * [2.4 Convert DS saves to LOA](#convert-ds-saves-to-loa)
   * [2.5 Enable EAX](#enable-eax)
   * [2.6 Enable LOA + Extras](#enable-loa--extras)
   * [2.7 Enable MP](#enable-mp)
   * [2.8 HD textures](#hd-textures)
   * [2.9 Import a character](#import-a-character)
   * [2.10 Increase shadow resolution](#increase-shadow-resolution)
   * [2.11 Increase UI size](#increase-ui-size)
   * [2.12 Install Mageworld, The Lands of Hyperborea and the Ultima 5/6 remakes on the Steam version](#install-mageworld-the-lands-of-hyperborea-and-the-ultima-56-remakes-on-the-steam-version)
   * [2.13 Play borderless fullscreen](#play-borderless-fullscreen)
   * [2.14 Play MP](#play-mp)
   * [2.15 Play MP map in SP](#play-mp-map-in-sp)
   * [2.16 Play windowed](#play-windowed)
   * [2.17 Play Yesterhaven map in SP](#play-yesterhaven-map-in-sp)
   * [2.18 Run the game above 1080p](#run-the-game-above-1080p)
   * [2.19 Use unsupported resolutions](#use-unsupported-resolutions)
* [3.0 Issues fixed](#issues-fixed)
   * [3.1 Black screen at Gom](#black-screen-at-gom)
   * [3.2 Booted back to the main menu after beating Gom](#booted-back-to-the-main-menu-after-beating-gom)
   * [3.3 Booted back to the MP menu when trying to host a game](#booted-back-to-the-MP-menu-when-trying-to-host-a-game)
   * [3.4 Cannot find world:global:vosounds in gas tree](#cannot-find-worldglobalvosounds-in-gas-tree)
   * [3.5 Crash/exception](#crashexception)
   * [3.6 Fuel failed to write file prefs.gas](#fuel-failed-to-write-file-prefsgas)
   * [3.7 Game freezes during cutscenes](#game-freezes-during-cutscenes)
   * [3.8 Game screen is offset](#game-screen-is-offset)
   * [3.9 Incompatible version](#incompatible-version)
   * [3.10 Lag in MP](#lag-in-mp)
   * [3.11 Mouse cursor is missing](#mouse-cursor-is-missing)
   * [3.12 Mouse cursor is stuck](#mouse-cursor-is-stuck)
   * [3.13 No GPU listed in DSVideoConfig](#no-gpu-listed-in-dsvideoconfig)
   * [3.14 Packmule inventory is inaccessible](#packmule-inventory-is-inaccessible)
   * [3.15 Poor performance](#poor-performance)
   * [3.16 Requested display mode is unsupported](#requested-display-mode-is-unsupported)
   * [3.17 Save failed](#save-failed)
   * [3.18 Shadows are missing](#shadows-are-missing)
   * [3.19 Some resources haven't been copied to the hard disk](#some-resources-havent-been-copied-to-the-hard-disk)
   * [3.20 Sorry, this save game was not created by Legends of Aranna and cannot be loaded](#sorry-this-save-game-was-not-created-by-legends-of-aranna-and-cannot-be-loaded)
   * [3.21 Steam detects the game as running after closing it](#steam-detects-the-game-as-running-after-closing-it)
   * [3.22 Stutters when moving the mouse](#stutters-when-moving-the-mouse)
   * [3.23 Textures are not loading](#textures-are-not-loading)
   * [3.24 UI/cursor flickering](#uicursor-flickering)
   * [3.25 Unable to create a new character](#unable-to-create-a-new-character)
   * [3.26 Unable to enumerate any DirectDraw devices installed on this system](#unable-to-enumerate-any-directdraw-devices-installed-on-this-system)
   * [3.27 Virtual alloc failed with error](#virtual-alloc-failed-with-error)
   * [3.28 White textures](#white-textures)
   * [3.29 Window is offscreen](#window-is-offscreen)
   * [3.30 Windows cursor flickers at the center of the screen](#windows-cursor-flickers-at-the-center-of-the-screen)
   * [3.31 You cannot run Dungeon Siege in a resolution higher than your desktop](#you-cannot-run-dungeon-siege-in-a-resolution-higher-than-your-desktop)
   * [3.32 Your hardware configuration is below minimum specification](#your-hardware-configuration-is-below-minimum-specification)
* [4.0 Modding](#modding)
   * [4.1 Cannot download GMAX when installing the toolkit](#cannot-download-gmax-when-installing-the-toolkit)
   * [4.2 D3D Initialization Failure](#d3d-initialization-failure)
   * [4.3 Make DSMod work on the Steam version](#make-dsmod-work-on-the-steam-version)
   * [4.4 Make DSLOAMod work on the Steam version](#make-dsloamod-work-on-the-steam-version)
   * [4.5 Make Siege Editor work on the Steam version](#make-siege-editor-work-on-the-steam-version)
   * [4.6 Remove a tank protection](#remove-a-tank-protection)
   * [4.7 Tank Creator doesn't work](#tank-creator-doesnt-work)
   * [4.8 View a protected tank](#view-a-protected-tank)
* [5.0 Walkthroughs](#walkthroughs)
* [6.0 Links](#links)
* [7.0 Credits](#credits)
* [8.0 Disclaimer](#disclaimer)

# Glossary

Shortcuts used throughout this document:

DS = Dungeon Siege  
GPU = Graphics Processing Unit (graphics card)  
LOA = Legends of Aranna  
MP = Multiplayer  
SP = Singleplayer  
\<config-file\> = "\<path-to-docs\>\DungeonSiege.ini"  
\<config-file-LOA\> = "\<path-to-docs-LOA\>\DungeonSiege.ini"  
\<gpu-model\> = actual name of your GPU (ex: "NVIDIA GeForce GTX 1070")  
\<mod-name\> = folder name of your mod (ex: u6p)  
\<path-to-docs\> = "%USERPROFILE%\Documents\Dungeon Siege"  
\<path-to-docs-LOA\> = "%USERPROFILE%\Documents\Dungeon Siege LOA"  
\<path-to-game\> = your installation directory (ex: "%PROGRAMFILES(X86)%\Steam\steamapps\common\Dungeon Siege 1")  

Please note that while this document is based on the Steam version (combined with [Killah's fix](#enable-loa--extras)), I did my best to accommodate retail users and those not using LOA. Some steps may be different and a few issues may not happen on the retail version.

# Guides

## Add the game on GameRanger

Method 1:

1. Download the [reg patch](https://github.com/GenesisFR/RegPatches) and run it from [\<path-to-game\>](#glossary) (select option 3).
3. In GameRanger, hit "Edit -\> Options -\> Games -\> Dungeon Siege -\> Browse" then select "DungeonSiege.exe" (the executable must be named "DSLOA.exe" for LOA) from Program Files:

   ![GameRanger](https://user-images.githubusercontent.com/3614449/119590524-eb99aa00-bda2-11eb-82ef-e7ab78bdcf35.png)

Method 2:

1. Download and run [Symlinker](https://amd989.github.io/Symlinker) (click on "Download Standalone Executable"). It's a front-end for the mklink command.
2. In Symlinker, make a directory junction to your game directory in Program Files:

   ![Symlinker](https://user-images.githubusercontent.com/3614449/119590493-dae93400-bda2-11eb-80a0-2d268d178814.png)

3. In GameRanger, hit "Edit -\> Options -\> Games -\> Dungeon Siege -\> Browse" then select "DungeonSiege.exe" (the executable must be named "DSLOA.exe" for LOA) from Program Files:

   ![GameRanger](https://user-images.githubusercontent.com/3614449/119590524-eb99aa00-bda2-11eb-82ef-e7ab78bdcf35.png)

Note: to change the game resolution, see method 1 or 3 of [Use unsupported resolutions](#use-unsupported-resolutions).

## Capture the game with OBS

I discovered a special trick to capture the game's window while playing fullscreen (without using desktop capture).

1. Run the game [windowed](#play-windowed).
2. Add a window capture in OBS and select DS (stretch it to fullscreen if you want).
3. Close DS and remove the launch parameter so it runs fullscreen.
4. Run the game again, OBS will still capture it.

If you're not playing at your native resolution, just make sure you don't alt-tab otherwise it'll fit only part of the screen! If you have to alt-tab, you can either go back to the main menu and load your saved game, or add a Crop/Pad filter (relative) on your window capture to remove the black borders.

If the game is not captured or listed in the drop-down menu at all, then I'd say you're either running the game in compatibility mode or as admin (OBS can't see processes with compatibility modes and won't list admin processes unless it's also run as admin). If it's not the case, then you're on a system with an integrated GPU and a dedicated GPU (like a laptop) and you may have to run the game on the same GPU that OBS is using.

Note: it also works with other games, as long as they're using DX9 (or older) or OpenGL.

## Change the FOV

Hex-edit the game's [executable](http://www.wsgf.org/dr/dungeon-siege).

## Convert DS saves to LOA

After installing LOA, you won't be able to load your DS saved games. You need to add a flag in each saved game for LOA to recognize your DS saved game by performing both steps below:

Decompile the save:

1. Download and run [Tank Viewer](https://www.siegetheday.org/?q=node/3044).
2. Click on Open, navigate to "[\<path-to-docs\>](#glossary)\Save" and select your save.
3. Click on Extract and select a folder (preferably empty) where to extract the files.
4. Open the "info.gas" file with a text editor.
5. Right below the line starting with "is_auto_save", add another line "is_dsx = true;".
6. Save the file.

Recompile the save:

1. Download and run [Tank Creator](https://www.zhixalom.com/lair/2005/09/12/tank-creator-2-1).
2. Click on Source and select the folder where you decompiled the files earlier.
3. Click on Output, select "[\<path-to-docs-LOA\>](#glossary)\Save" and make sure the file has a DSSAVE extension.
4. Select "DS & LOA" under Format.
5. Click on Create (if nothing happens, see [Tank Creator doesn't work](#tank-creator-doesnt-work)).

You should now be able to load your save in LOA. The inventory of your mules may become glitched though (see [Packmule inventory is inaccessible](#packmule-inventory-is-inaccessible)).

If you prefer a visual guide, see [this](https://steamcommunity.com/sharedfiles/filedetails/?id=2218528449).

Source: https://discordapp.com/channels/373223103985090581/400744824593973248/587998587112259584

## Enable EAX

1. Download [dsoal](https://pcgamingwiki.com/wiki/Glossary:Sound_card#Universal_2).
2. Extract dsound.dll and dsoal-aldrv.dll to [\<path-to-game\>](#glossary).
3. Run the game and enable EAX in the options.

## Enable LOA + Extras

Follow the instructions from [Killah's guide](https://steamcommunity.com/sharedfiles/filedetails/?id=1148174213).

## Enable MP

If Windows doesn't detect that the game needs DirectPlay (when clicking on Multiplayer), go to Control Panel -\> Programs and Features -\> Turn Windows features on or off -\> Legacy Components -\> Enable DirectPlay.

Note: this only applies to Windows 7 or later.

## HD textures

There are currently two HD textures packs available.

The first one (recommended) is a set of [upscaled textures](https://www.nexusmods.com/dungeonsiege1/mods/44) (based on the original) using ESRGAN by Antrad2020.

The second one is a set of [textures](https://www.mediafire.com/file/7awhevfmqochnpo/Dungeon_Siege+-+Legendary+textures.zip) from the Legendary Mod (a DS2 mod that ports DS1 content over the DS2 engine) ripped by Eksevis.

Note: it seems to work fine on all custom campaigns and doesn't bloat saves (only tested in The Lands of Hyperborea and the Ultima remakes).

## Import a character

If you want to import an existing character into a single player game, do the following.

1. Download Siege Editor and install it.
2. Load your latest save and save it again with a simple name (ex: "X").
3. Run the game again through DSMod or DSLOAMod. They enable the in-game console.
4. Start a brand-new single player game.
5. Bring down the console (~), point the cursor at a wide-open patch of ground, and run this command: party load X.dssave

## Increase shadow resolution

Open "[\<path-to-game\>](#glossary)\system_detail.gas" and change the 10 occurrences of "shadow_tex_size	= 64" to 128/256/512/1024. You can do a search and replace on "= 64".

Note: 512 and above can be VERY taxing when using the "All complex" setting, especially in forests (in that case, switch to "Party complex"). Values higher than 1024 (or 256 for DSLOAMod) may prevent the game from loading.

## Increase UI size

If you play the game at higher resolutions (like 1080p), the UI won't scale and will become tiny. There is a workaround that involves rendering the game at a specific resolution and the UI at a lower resolution (effectively making it bigger):

1. Install [dgVoodoo2](https://www.pcgamingwiki.com/wiki/DgVoodoo_2#DirectX_1-7).
2. Run dgVoodooCpl.exe, go to the DirectX tab, select your native resolution from the Resolution drop down list and hit OK.
3. Set the game at the resolution you want the UI to be scaled to, typically 720p or lower (see [Use unsupported resolutions](#use-unsupported-resolutions)).

Note: these instructions won't work while running the game in windowed mode.

## Install Mageworld, The Lands of Hyperborea and the Ultima 5/6 remakes on the Steam version

Normally, the Ultima remakes are meant for the retail version, but some people made guides to make them work on the Steam version:

- https://dor-lomin.com/2016/04/30/running-the-ultima-6-project-on-a-steam-edition-of-dungeon-siege (or use the [reg patch](https://github.com/GenesisFR/RegPatches))
- https://www.projectbritannia.com/forum/index.php?topic=2446.msg16746#msg16746

I made some drag-and-drop archives if you want to skip the installation guide above:

- https://www.mediafire.com/file/ik093jdkkvle066/Ultima_V_-_Warriors_of_Destiny.zip
- https://www.mediafire.com/file/4xvcewat7ctpjvd/Ultima_VI_-_The_False_Prophet.zip

For the other mods, just ignore the above and download these archives:

- https://www.mediafire.com/file/48lcyx22nqzbd5h/Dungeon_Siege_-_Mageworld.zip
- https://www.mediafire.com/file/qh4d2l5a46cd1g7/Dungeon_Siege_-_The_Lands_of_Hyperborea.zip

Please follow these steps for each mod to make sure everything is working properly:

1. Extract the archive to your DS folder.
2. Edit the provided BAT file with your desired resolution.
3. Copy the content of [\<path-to-docs\>](#glossary) to the "[\<path-to-game\>](#glossary)\\\<mod-name>\User\Save" subfolder prior to running the mod (if you'd like to keep your key bindings and game preferences).
4. Run the mod with the BAT file (you can also replicate its arguments in a shortcut or Steam launch options).
5. Saved games will be located under the "[\<path-to-game\>](#glossary)\\\<mod-name>\User\Save" subfolder (to avoid overriding saves from the main game). 

Note: all of these mods are NOT compatible with LOA. Please refer to their respective readme files for further issues.

## Play borderless fullscreen

There are multiple programs that allow games to run borderless fullscreen (you can find an exhaustive list [here](https://www.pcgamingwiki.com/wiki/Glossary:Borderless_fullscreen_windowed)), however for the sake of simplicity, we'll only cover one of them here.

1. Download [Fullscreenizer](https://github.com/KasumiL5x/Fullscreenizer/releases) and run it.
2. Run the game in [windowed](#play-windowed) mode.
3. Switch back to Fullscreenizer.
4. If the game doesn't appear in the list, click on "Show All", select "Dungeon Siege" and click on "Add".
5. Select the game in the list and press the Fullscreenize button (or use your hotkey combination), preferably after loading a game (see note below).

Note: the main menu UI has a fixed resolution and will be broken, repeat step 5 again to make the game windowed again. The game may randomly freeze when switching windowed modes so try to avoid it.

## Play MP

Run the game with the "zonematch=true" launch parameter to directly boot into the MP menu (not necessary if you're using the retail version or [Killah's fix](#enable-loa--extras)).

## Play MP map in SP

Install one of these mods:

- [Legends of Utrae](https://www.siegetheday.org/?q=node/1317) (recommended)
- [Myros](https://www.fileplanet.com/87368/80000/fileinfo/Myros-Mod) (or use this [link](https://www.dropbox.com/sh/utwgyv8ic6bpyd2/AADp6em9zEbh9Bo-gCfxSYy3a/myrosmap.zip))

## Play windowed

Add the "fullscreen=false" launch parameter (see the following instructions for [shortcuts](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#Desktop_shortcuts), [Steam](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#Steam) or [GOG Galaxy](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#GOG_Galaxy_2.0)) or in the config file (see method 3 of [Use unsupported resolutions](#use-unsupported-resolutions)).

## Play Yesterhaven map in SP

I made a drag-and-drop [archive](https://www.mediafire.com/file/tk4qfvq2gqb217r/Dungeon_Siege_-_YesterhavenSP.zip) from [Father Bronze's Yesterhaven Single-Player Edition](http://ds.gemsite.org/web/index.php/maps/map-addons/GET/detail-61) so you won't have to worry about resources conflicting with each other.

Just extract it to your DS folder and use the provided BAT file to run the mod.

## Run the game above 1080p

Check the "dgVoodoo for 1920x1080+ resolutions" section in [Beatlebattle's guide](https://steamcommunity.com/sharedfiles/filedetails/?id=1642475147#2897971).

You'll need [dgVoodoo2](https://www.pcgamingwiki.com/wiki/DgVoodoo_2#DirectX_1-7).

## Use unsupported resolutions

By default, the game can only be played in 640x480, 800x600 or 1024x768.

However, with some tweaking, you can play it at any resolution. There are a few caveats though:

- the UI doesn't scale up (see [Increase UI size](#increase-ui-size) for a workaround)
- there are (supposedly) glitches in cutscenes
- a warning message (that can safely be ignored) will appear when starting/loading a game (see [Requested display mode is unsupported](#requested-display-mode-is-unsupported) to remove it)

You have 4 ways to make the game run at custom resolutions.

Method 1 (recommended):

1. Download [SeeFar 2020](https://www.nexusmods.com/dungeonsiege1/mods/45).
2. Open the downloaded archive and navigate to the "ResolutionFix" subfolder.
3. Extract "system_detail.gas" to [\<path-to-game\>](#glossary) (it does the same thing than [Requested display mode is unsupported](#requested-display-mode-is-unsupported)) and "sf_ResolutionFix.dsres" to "[\<path-to-game\>](#glossary)\Resources".
4. Run the game.
5. Select your desired resolution from the options.

Method 2:

Add the "width=xxxx" and "height=xxxx" launch parameters (where "xxxx" is your desired resolution, for instance "width=1920 height=1080"). See the following instructions for [shortcuts](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#Desktop_shortcuts), [Steam](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#Steam) or [GOG Galaxy](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#GOG_Galaxy_2.0).

Method 3:

1. Open [\<config-file\>](#glossary) (or [\<config-file-LOA\>](#glossary) for LOA) with a text editor.
2. Change the "width = xxxx" and "height = xxxx" to your desired resolution (where "xxxx" is your desired resolution).
3. Save the file.

Method 4:

1. Follow the steps described in [Requested display mode is unsupported](#requested-display-mode-is-unsupported).
2. Run "[\<path-to-game\>](#glossary)\DSVideoConfig.exe" and select your custom resolution.
3. Copy "[\<path-to-game\>](#glossary)\DungeonSiege.ini" to [\<path-to-docs\>](#glossary) (or [\<path-to-docs-LOA\>](#glossary) for LOA).

It's better to specify the resolution in launch parameters (method 2) compared to the configuration file (method 3 and 4) because it will prevent the game from changing it back to the default resolutions while navigating the options menu.

Note: for resolutions higher than 1080p, check [Run the game above 1080p](#run-the-game-above-1080p).

# Issues fixed

## Black screen at Gom

When going down the elevator before fighting Gom, the cutscene may break and pressing Escape will trigger a black screen. This bug is caused by the camera script that comes with LOA, which doesn't work properly when SeeFar is installed. It breaks one of the camera triggers during that cutscene, preventing it from completing.

There are 2 ways to circumvent it.

Method 1 (recommended):

1. Download this [hotfix](https://www.mediafire.com/file/auqjxy62co40tjh/koe_camera_hotfix.dsres).
2. Place it in "[\<path-to-game\>](#glossary)\Resources".
3. Run the game.
4. Load your saved game.
5. Proceed to beat Gom.
6. Remove the hotfix (otherwise the initial cutscene of the LOA campaign will break).

Method 2:

You have to import your party from your modded save to another save that doesn't use SeeFar. For your convenience, you can download an unmodded saved game right before Gom [here](https://www.mediafire.com/file/3djao9ez7nkpv3m/endgame_save.dssave).

1. Place the unmodded save into [\<path-to-docs-LOA\>](#glossary)\Save.
2. Run DSLOAMod (see [Make DSLOAMod work on the Steam version](#make-dsloamod-work-on-the-steam-version)).
3. Ignore all the errors it may throw.
4. Load the "endgame_save" saved game.
5. Open the console with ~ (or the key above TAB).
6. Place the mouse cursor on flat ground, between your characters.
7. Type "party load \<name-of-your-save\>.dssave".
8. Check that all your characters are there.
9. Proceed to beat Gom.

Note: if you save again, your new saved game will only be accessible from DSLOAMod.

## Booted back to the main menu after beating Gom

The multiplayer and anything related to it was disabled in the Steam version. Use [Killah's fix](#enable-mp).

Note: you'll need to [convert your save to LOA](#convert-ds-saves-to-loa).

## Booted back to the MP menu when trying to host a game

- Enable DirectPlay (see [Enable MP](#enable-mp)).
- Add the "dpnsvr=false" launch parameter (see the following instructions for [shortcuts](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#Desktop_shortcuts), [Steam](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#Steam) or [GOG Galaxy](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#GOG_Galaxy_2.0)).

## Cannot find world:global:vosounds in gas tree

Your game files are corrupted. Reinstall the game.

## Crash/exception

It can be caused by literally anything. Here are a few common fixes I've gathered since I started playing this game:

- Use simple shadows (Options -\> Shadows -\> Simple) or disable them.
- Lower object quality (Options -\> Object Detail).
- Use [dgVoodoo2](https://www.pcgamingwiki.com/wiki/DgVoodoo_2#DirectX_1-7).
- Run the game as administrator.
- Run the game in compatibility mode (try all of them).
- Run the game from the executable instead of Steam.
- Run the game on your other GPU (if you have one).
- If you're using a resolution higher than 1080p, see [Run the game above 1080p](#run-the-game-above-1080p).
- Disable overlays (Steam, GOG, Discord, etc).
- Right-click "DungeonSiege.exe" then hit "Properties -> Compatibility -> Reduced color mode -> 16-bit (65536) color".
- One of your saved games is corrupted, remove it.
- Some mods can conflict with each other. Find and remove conflicting mods.
- Some mods don't work with LOA. Find and remove incompatible mods, then look for similar mods compatible with LOA.
- Make the game recognize your GPU with this [guide](https://steamcommunity.com/sharedfiles/filedetails/?id=780048558).
- Make sure the "My Documents" directory is on your C drive.
- Run "[\<path-to-game\>](#glossary)\DSVideoConfig.exe" and switch your driver to "[\<gpu-model\>](#glossary) - Hardware" (or its TnL equivalent).
- Lower your shadow resolution to 256, see [Increase shadow resolution](#increase-shadow-resolution).
- Install [DirectX 9.0c](https://www.microsoft.com/en-us/download/details.aspx?id=8109).

Note: DSVideoConfig only edits "[\<path-to-game\>](#glossary)\DungeonSiege.ini" (it's intended to be run before playing the game the first time) so make sure to copy it to [\<path-to-docs\>](#glossary) (or [\<path-to-docs-LOA\>](#glossary) if you're using LOA).

## Fuel failed to write file prefs.gas

- Run "[\<path-to-game\>](#glossary)\DSVideoConfig.exe" as administrator.
- Make sure [\<path-to-docs\>](#glossary) is not read-only.
- Disable your anti-virus.

Source: https://www.facebook.com/photo.php?fbid=710028262735915

## Game freezes during cutscenes

This may be caused by the game unable to teleport your other characters if they're in another region. Make sure all your characters are close to each other before triggering a cutscene.

## Game screen is offset

If your game looks zoomed in, it's likely caused by your screen scaling settings.

1. Right-click "DungeonSiege.exe" then hit "Properties".
2. Go to "Compatibility -\> Change high DPI settings".
3. Check "Override high DPI scaling behaviour" and make sure "Application" is selected in the drop-down menu.

Alternatively, you can set the Windows display scaling setting back to 100%:

1. Right-click on your desktop.
2. Select "Display settings".
3. Go to "Scale and layout".
4. Select "100% (Recommended)".

Source: https://steamcommunity.com/app/39190/discussions/0/620696522225972749/#c1642038749323053918

## Incompatible version

When playing MP, it's important that everyone uses EXACTLY the same files.

The game performs a CRC check on all files. If check values between clients don't match, the game won't let you join someone else's game. It's often caused by different executables, resources and game language. Even an additional resource (typically a mod) will cause it.

Here are the files that differ between the Steam and retail versions:

- Resources\DevLogic.dsres
- Resources\Logic.dsres
- Resources\Objects.dsres
- DungeonSiege.exe

You can get the Steam version of these files [here](https://www.mediafire.com/file/hxvnxxqlmmiheeh/Dungeon_Siege_Steam_resources.zip).

Here are the files that differ between languages:

- DSLOA\ExpVoices.dsres (retail only)
- Resources\Language.dsres
- Resources\Voices.dsres (retail only)
- Language.dll

## Lag in MP

This can be caused by dgVoodoo2. Potential fixes include:

- Running the game without it.
- Running the game on LAN.
- Running the game on LAN through a VPN-like software (ex: Hamachi, ZeroTier).

## Mouse cursor is missing

Turn off supersampling in your GPU control panel.

For NVIDIA users:

1. Right-click on your desktop.
2. Select "NVIDIA Control Panel".
3. Click on "Manage 3D settings".
4. Set "DSR - Factors" to "Off".

For AMD users:

1. Right-click on your desktop.
2. Select "AMD Radeon Settings".
3. Click on the "Display" tab.
4. Set "Virtual Super Resolution" to "Off".

Source: https://steamcommunity.com/app/39190/discussions/0/612823460274990833#c617328415054371674

## Mouse cursor is stuck

Disable DPI scaling. Follow the same instructions as in the "[game screen is offset](#game-screen-is-offset)" section.

Source: https://steamcommunity.com/app/39190/discussions/0/3192485835693148901

## No GPU listed in DSVideoConfig

- [Enable DirectDraw acceleration](https://superuser.com/a/504510).
- Follow [doa_92's guide](https://steamcommunity.com/sharedfiles/filedetails/?id=780048558).

## Packmule inventory is inaccessible

After converting a DS save to LOA, packmules are being treated like traggs (8 * 13 cells) but the UI remains the one from the mule (12 * 13 cells). Therefore, you can't access the items located in the last 5 columns.

You have to remove items from your mule's inventory and hit the "Auto-arrange inventory" button to be able to access them.

## Poor performance

Run the game once then open [\<config-file\>](#glossary) (or [\<config-file-LOA\>](#glossary) for LOA) with a text editor. Make sure you have the following at the top:

```
driver_description = <gpu-model> - Hardware
width = 1024
height = 768
bpp = 32
bltonly = true ; highly recommended
```

You can also add this too, if you want:

```
nointro = true ; skips the intro logo
fullscreen = false ; makes the game windowed
maxfps = 62 ; limits the framerate
```

If the game still doesn't run well, you may want to run it on your other GPU (if you have one) or add your GPU to the list so the game recognizes it (see [No GPU listed in DSVideoConfig](#no-gpu-listed-in-dsvideoconfig)).

Note: if the framerate is bad in windowed mode, applying the fixes from [UI/cursor flickering](#uicursor-flickering) may help.

## Requested display mode is unsupported

When running the game in resolutions other than the default ones, a warning message will be displayed every time you start/load a game from the main menu.

Open "[\<path-to-game\>](#glossary)\system_detail.gas" and everywhere you see 1024x768, add a duplicate of that line but change it with your resolution, like in the example below:

```
[resolutions]
{
	[640x480]	{ max_back_buffers = 1; }
	[800x600]	{ max_back_buffers = 1; }
	[1024x768]	{ max_back_buffers = 2; }
	[1280x720]	{ max_back_buffers = 2; }
	[1920x1080]	{ max_back_buffers = 2; }
}
```

## Save failed

When trying to save the game, you may get a message saying "Save failed" and no save is created under [\<path-to-docs\>](#glossary).

- Your antivirus/antimalware/ransomware protection is at fault. Add the game as an exception or disable it.
- You have a username with special (non-latin) characters. Change your username so it only uses latin characters.
- Run the game as admin.

Note: it happens in a few other games too.

Source: https://steamcommunity.com/app/39200/discussions/0/2619339453457265287

## Shadows are missing

This is caused by setting "shadow_tex_size" too high for DSMod/DSLOAMod, thus preventing them from working. DSMod/DSLOAMod don't support anything above a resolution of 256, therefore set "shadow_tex_size" to 256 or less. Besides, DSLOAMod crashes with shadow resolution set above 256.

## Some resources haven't been copied to the hard disk

You're missing some core files (most likely "[\<path-to-game\>](#glossary)\Resources\logic.dsres"). Reinstall the game.

## Sorry, this save game was not created by Legends of Aranna and cannot be loaded

See [Convert DS saves to LOA](#convert-ds-saves-to-loa).

## Steam detects the game as running after closing it

This may happen after hosting/joining a multiplayer session.

1. Open Task Manager.
2. Go to the Details tab.
3. Find dpnsvr.exe and terminate it.

## Stutters when moving the mouse

- Disable any kind of frame limiter.
- Disable any kind of vertical synchronization (including in dgVoodoo2) and FreeSync/G-Sync.
- This was also caused by the NVIDIA drivers for Cyberpunk (460.79). The problem was fixed in 466.11 (and again in 497.29). If it's still not fixed for you for some reason, use older or newer drivers. You may find them using this [link](https://www.nvidia.com/Download/Find.aspx?lang=en-us) or this [one](https://www.nvidia.in/drivers/beta).

## Textures are not loading

This is caused by using the HD textures mod with DSMod/DSLOAMod, therefore making most of the world transparent. DSMod/DSLOAMod don't support anything above a resolution of 256 so you have remove the mod.

## UI/cursor flickering

- Right-click "DungeonSiege.exe" then hit "Properties -\> Compatibility -\> Reduced color mode -\> 16-bit (65536) color".
- Make sure it says "bpp = 32" in [\<config-file\>](#glossary) (or [\<config-file-LOA\>](#glossary) for LOA).
- Disable any kind of antialiasing in your GPU driver settings.
- Press the Windows key to minimize the game then maximize it.
- Run the game on your other GPU (if you have one).
- Run the game in fullscreen or [windowed](#play-windowed) mode.

## Unable to create a new character

If you're experiencing missing animations or freezes in the character creator, this may be caused by third party softwares such as XFire or Raptr. You should disable them or uninstall them as they've been discontinued a long time ago.

## Unable to enumerate any DirectDraw devices installed on this system

[Enable DirectDraw acceleration](https://superuser.com/a/504510).

## Virtual alloc failed with error

The game is running out of memory. It's usually due to using memory intensive mods such as the HD textures.

Make the game's executable large-address aware using the [LAA enabler](https://www.pcgamingwiki.com/wiki/Windows#Set_older_32-bit_games_to_use_4_GB_RAM_instead_of_2) so it can use more RAM.

## White textures

This usually happens when using dgVoodoo2.

1. Run dgVoodooCpl.exe, go to the General tab and select one of the Direct3D 12 entries from the Output API drop down list.
2. Go to the DirectX tab, tick "Fast memory access" and hit OK.
3. Decrease [shadow resolution](#increase-shadow-resolution) to 512 or lower.
4. If you're using an AMD GPU, turn off [Radeon Anti-Lag](https://www.amd.com/en/support/kb/faq/dh-033#faq-Configuring-Radeon-Anti-Lag).

## Window is offscreen

Add "x=0 y=0" to your launch parameters (see the following instructions for [shortcuts](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#Desktop_shortcuts), [Steam](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#Steam) or [GOG Galaxy](https://www.pcgamingwiki.com/wiki/Glossary:Command_line_arguments#GOG_Galaxy_2.0)).

Source: https://steamcommunity.com/app/39200/discussions/0/846955554677340085/#c1692669912401473624

## Windows cursor flickers at the center of the screen

It's likely caused by using dgVoodoo2, just tab out of the game and tab back in.

## You cannot run Dungeon Siege in a resolution higher than your desktop

Lower the game's height (see [Use unsupported resolutions](#use-unsupported-resolutions)) so that it corresponds to your desktop's height minus at least 40 pixels (it can be more) to account for the borders (ex: 1920x1080 -\> 1920x1040).

## Your hardware configuration is below minimum specification

Add your GPU to "[\<path-to-game\>](#glossary)\system_detail.gas" with this [guide](https://steamcommunity.com/sharedfiles/filedetails/?id=780048558).

# Modding

## Cannot download GMAX when installing the toolkit

You can get GMAX from [here](https://archive.org/details/gmax-1.2-with-registration-key).

## D3D Initialization Failure

Replace preferences.gas in "[\<path-to-docs\>](#glossary)\Editor" with this [one](https://www.mediafire.com/file/pj3bzqg42pqvdti/preferences.gas).

## Make DSMod work on the Steam version

TLDR (both scenarios): https://www.mediafire.com/file/852l283dl7p580j/DSMod_Steam_version.zip

Download the [reg patch](https://github.com/GenesisFR/RegPatches) and run it from [\<path-to-game\>](#glossary) to make DSMod find your game.

After doing that, you will run into two scenarios depending on which reg patch you were using prior to installing the toolkit.

Scenario 1:

If you were using an old version of the reg patch (an executable), the "DSMod.exe" QA version (02.12.1603) won't match Steam's "DungeonSiege.exe" QA version (03.07.0202), so you'll need to use a tool like [Resource Hacker](https://portableapps.com/apps/utilities/resource-hacker-portable) to make them identical:

1. Make a backup of "DSMod.exe" (just in case).
2. Run two instances of Resource Hacker as administrator.
3. In the first instance, hit "File -\> Open -\> DSMod.exe".
4. In the second instance, hit "File -\> Open -\> DungeonSiege.exe".
5. In both instances, hit "Version Info -\> 1 : 1033".
6. Locate the line "MSQAVersion" and replace its value in "DSMod.exe" by the value from "DungeonSiege.exe".
7. Click on the green arrow (or F5) to compile the script.
8. Click on the green floppy disk (or Ctrl + S) to save the file.

Scenario 2:

If you were using the new version of the reg patch (a batch script), DSMod will ask for disc 1 of LOA. Download and mount the mini image from [Make DSLOAMod work on the Steam version](#make-dsloamod-work-on-the-steam-version).

Note: see [Shadows are missing](#shadows-are-missing) and [Textures are not loading](#textures-are-not-loading) for potential issues.

## Make DSLOAMod work on the Steam version

Download the [reg patch](https://github.com/GenesisFR/RegPatches) and run it from [\<path-to-game\>](#glossary) to make DSLOAMod find your game.

DSLOAMod won't get installed unless LOA is installed. On top of that, it uses SmarteSecure DRM disc check so you'll need to have disc 1 of LOA in your disc drive or it'll refuse to run.

If you don't want to go this route, I created a [mini image](https://www.mediafire.com/file/a7cxee61t49v17f/DSLOA1+mini+image.iso) that will satisfy the disc check.

Just mount the ISO with Windows File Explorer or with a third party software (like WinCDEmu) before running DSLOAMod.

If you have a "Couldn't register file.tmp" popup followed by a SmarteSecure popup, it means the location you're trying to run it from has permission issues. Run DSLOAMod as admin or move it elsewhere.

You may also have a few "ATLCOMHelper Exception" popups. You can safely ignore those and DSLOAMod will run. To get rid of them, either use the DSLOAMod shortcut in the toolkit installation directory, place DSLOAMod in [\<path-to-game\>](#glossary) and run it from there, or open Task Manager and end the task for "Protection Stub (32-bit)".

Also, if you're running DSLOAMod from a shortcut, you may have to run it without admin privileges.

Note: see [Shadows are missing](#shadows-are-missing) and [Textures are not loading](#textures-are-not-loading) for potential issues.

## Make Siege Editor work on the Steam version

Download and run the [reg patch](https://github.com/GenesisFR/RegPatches) from [\<path-to-game\>](#glossary) to make the editor find your game.

To fix the "Unable to find video card entry for your hardware" warning in Siege Editor, you need to add an entry corresponding to your GPU in "[\<path-to-game\>](#glossary)\system_detail.gas". The device name and both IDs are shown in the error message and must be prefixed with "0x".

Where you add it is important, otherwise it may disable some effects (like complex shadows). Look up the section corresponding to the vendor of your graphics card (nVidia, ATI or Intel). In my case, I added this entry at the beginning of the "nVidia" vendor section (before the other "[device*]" entries):

```
[device*]
{
	name					= "GeForce GTX 1070";
	x vendorid				= 0x10de;
	x deviceid				= 0x1b81;
	x driver_product		= 0;
	x driver_version		= 0;
	b trilinear_filt		= true;
	b shadow_render_target	= true;
}
```

As a bonus, setting "shadow_render_target" to true seems to increase the framerate while using complex shadows (at least on my system). It can be used when not modding too!

You can ignore the "xp_" warnings when starting the editor (they'll pop up if you installed [Killah's fix](#enable-loa--extras)). If you wish to get rid of them, you have to (re)move the "Return to Arhok" campaign. To do so, move/delete the following files:

- "[\<path-to-game\>](#glossary)\Maps\XPMap.dsmap"
- "[\<path-to-game\>](#glossary)\Resources\XPRes.dsres"

Note: setting "shadow_tex_size" higher than 256 will yield another warning that can safely be ignored and using the HD textures mod will make them white.

## Remove a tank protection

1. Open your protected tank with an Hex Editor.
2. Go to offset 38 and replace 04 by 00.
3. Save the file.

Source: https://www.facebook.com/groups/DungeonSiegeForever/permalink/814904645815105/?comment_id=814930495812520

## Tank Creator doesn't work

If nothing happens when clicking on the Create button in Tank Creator, make sure it's added to the exclusion list of your antivirus. If that still doesn't work, add your TEMP directory to the exclusion list as that's where RPC (the underlying program to Tank Creator) is executed from.

## View a protected tank

1. Open Siege Editor.
2. Hit "Siege Editor -\> File -\> Convert .dsmap to Files...".
3. Select your DSRES/DSMAP from the "Source File" button.
4. Uncheck "Use default destination folder" and select the folder where you want to extract it (if it's checked, the default destination folder is "[\<path-to-docs\>](#glossary)\Bits").
5. Uncheck "Extract .lqd files" if you just want to view the extracted files.
6. Click OK.

# Walkthroughs

All-in-One:

- https://steamcommunity.com/sharedfiles/filedetails/?id=1264921426

DS:

- http://ds.gemsite.org/web/index.php/kingdom-of-ehb
- https://www.walkthroughking.com/text/dungeonsiege.aspx

LOA:

- http://ds.gemsite.org/web/index.php/legends-of-aranna
- https://www.walkthroughking.com/text/dungeonsiegearanna.aspx

Utraean Peninsula:

- http://ds.gemsite.org/web/index.php/utraen-peninsula

# Links

- https://discord.gg/PPsdY3D (unofficial community Discord)
- http://ds.gemsite.org/web/index.php/main
- http://ds-old.gemsite.org
- http://ds.heavengames.com
- http://ds2.bplaced.net/sysdat/ds1 ("system_detail.gas" configurator)
- http://dungeonsiege.8m.net/train_univer.htm (modding documentation)
- https://dungeonsiege.fandom.com/wiki/Dungeon_Siege (DS wiki)
- https://dungeonsiege.fandom.com/wiki/Dungeon_Siege:_Legends_of_Aranna (LOA wiki)
- https://www.facebook.com/groups/DungeonSiegeForever (unofficial Facebook page)
- https://www.gamefront.com/games/dungeon-siege (DS mods)
- https://www.gamefront.com/games/dungeon-siege-legend-of-aranna (LOA mods)
- https://www.moddb.com/games/dungeon-siege (DS mods)
- https://www.moddb.com/games/dungeon-siege-legend-of-aranna (LOA mods)
- https://www.nexusmods.com/dungeonsiege1 (mods)
- https://www.siegetheday.org (unofficial community)
- https://sites.google.com/view/chickengeorgemods/modding (modding tools)
- https://steamcommunity.com/groups/TheKingdomOfEhb (Steam group)
- http://www.trogworld.com/ds.htm (DS mods)
- https://www.zhixalom.com/lair/category/dungeon-siege-1 (DS/LOA mods)

# Credits

This document wouldn't have been possible without the following people:

- .orix (Discord) - lots of fixes
- [0xff](https://www.twitch.tv/0xff2)
- [Ahrimotto](https://www.reddit.com/user/Ahrimotto)
- [AlceX](https://steamcommunity.com/id/alcex) - freezing cutscene fix
- [Antrad2020](https://antonior-software.blogspot.com)
- Azlaroc - 100$ donation
- bawnerbaw (Discord) - save conversion guide
- [Beatlebattle](https://steamcommunity.com/id/beatlebattle)
- coop13 (Discord) - white texture fix
- [doa_92](https://steamcommunity.com/id/doa_92)
- eksevis (Discord)
- Father Bronze - SP version of Yesterhaven
- [lgrzinc](https://steamcommunity.com/profiles/76561198097266688) - character creator fix
- Killah - LOA guide and DS community
- sadowson (Discord) - lots of fixes
- [Soban](https://steamcommunity.com/id/S0BAN) - save conversion guide
- starfalll (Discord) - lots of fixes
- The Walkthrough King
- [Tiberius](https://steamcommunity.com/profiles/76561197978671411)
- tristanzz (Discord) - import character guide
- [Tyler799](https://github.com/Tyler799) - format used for this guide

And the following resources:

- https://pcgamingwiki.com/wiki/Dungeon_Siege
- https://pcgamingwiki.com/wiki/Dungeon_Siege:_Legends_of_Aranna
- http://www.wsgf.org/dr/dungeon-siege
- GOG forums
- Steam Community forums/guides

Thanks a lot for your help!

# Disclaimer

I won't be held responsible if you mess up your game or saved game after using one of these fixes. You do it at your own risk!

You're not allowed to put this document in raw form anywhere, out of respect (it took me over 5 years to compile it). Just share the GitHub link or redirect users to this [thread](https://steamcommunity.com/app/39190/discussions/0/1813170373233918779).
