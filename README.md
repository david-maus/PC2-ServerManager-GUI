# **Project Cars 2 Dedicated Server Wrapper**
[GEF-GAMING.DE](http://www.gef-gaming.de)
---
![alt text](https://i.imgur.com/SefJeD7.png)
## **Server starter / Weather randomizer / Configurable per .ini**
**Just install the dedicated server, get the wrapper, make your inis and start the server**

**No more editing or copy configs for certain functions on serverupdate / fresh install / steam file verify**

*** ------Linux support coming soon / Video & Pictured tutorial coming soon------***

The Dedicated Server Wrapper is a little tool  that allows you to configure your
Project Cars 2 Server on a per .ini base.
Instead of edit and configure all the different files for the server
(server.cfg, rotatefile, motd, statsfile etc.) you can configure a session with
just one single .ini file.

You can make infinite .ini files / server configurations. Without edit the server files again and again.

One of the main features is the weather randomizing. You can set the chance in % for the possible weather states (You can of course deactivate things like snow, storm etc.). The wrapper fills the weatherslots randomly, based on your chance settings after every serverstart (If you activate it).

For authentic weather you can activate the option "AuthenticWeather". With this option
the first QualifySlot is the same as the last PracticeSlot and the first RaceSlot is the same as
the last QualifySlot. No more complete weather change from one session to another.

---

## **Features**

- All Server and Session settings comfortable in one single .ini file
- Multiple .ini files for infinite server/session setups
- MaxGrid / MaxPlayers automatic to max possible for a track
- Helper files for all possible Tracks and Vehicleclasses
- Implemented Serverrestart after X Minutes if you want
- Easier Multiclass setup
- Classmode to deactivate the class restriction (All cars possible, for Trackday / Tourist servers)
- Racelenght setup in one line (10L for 10 laps or 10M for 10 minutes timed race)
- Startscript Generator for all your created .ini files / server settings / session. Just create all your league rounds and get the correct startscripts with one click.
- And many many many more. You can easy setup every possible Value in the ini files

- **Randomized Weather with chance in %**
    - AuthenticWeather for plausible sessionchange (Pr to Q to R)
    - Override the weather to 1 Clear Slot for every Session (If the server is bugging with weather changes, its the case at the moment - 10. March 2018) with "Sunshine" Mode


- **PracticeServer Mode** (For Practicing the same ini/track under the week, for example in leagues)
 - *Overrides the ini configuration to:*
    - 24H practice and qualify session, 1 Lap race
    - No license
    - Weatherprogression to realtime
    - Dateprogression to OFF
    - deactivates mandatory Pitstop


- PracticeServer and Sunshine Mode can be overwritten through startparameters (Just use your correct leage/cup/race ini)


- **Automatic file copy to serverdirectory on start**
 - On every serverstart get the correct and fresh server.cfg / rotateFile / motd / baseFile / statsConfig
 - For use with simresults or other services, the current stats data is deleted before every start
 - For use with simresults or other services, the sessionTracking is activated before every start
 - Edited motd (No WeatherSlots Info in Lobbychat)


- **Just install the dedicated server, get the wrapper, make your inis and start the server**
- **No more editing or copy configs for certain functions on serverupdate / fresh install / steam file verify**
---
### ** Thanks to [MortICi](http://forum.projectcarsgame.com/member.php?3295-MortICi) for the sms_base.lua / sms_motd.lua Files and his work on the dedicated server configs!**
[His awesome Thread for the dedicated server configs](http://forum.projectcarsgame.com/showthread.php?56669-Dedicated-Server-Configuration-Sample-Weather-MultiClass-REALLY-FIXED!-2-25-18)

---

## **How to install**

1. Download the ServerWrapper [here](https://bitbucket.org/david-maus/gef-gaming.de_pc2-ds-wrapper/downloads/)
2. Copy / Extract the folder to your Dedicated Server root directory:

 Examplepath:

 `C:\_GAMES\Steam\steamapps\common\Project CARS 2 - Dedicated Server`

 After copy:

 `C:\_GAMES\Steam\steamapps\common\Project CARS 2 - Dedicated Server\gef-gaming.de_pc2-ds-wrapper`

---

## **How to use / Standard**

1. In the configs folder:

    `C:\_GAMES\Steam\steamapps\common\Project CARS 2 - Dedicated Server\gef-gaming.de_pc2-ds-wrapper\configs`

    You find a `basic.ini`
2. Edit this file for your server/session
3. Start the server under:

    **Windows**

    `C:\_GAMES\Steam\steamapps\common\Project CARS 2 - Dedicated Server\gef-gaming.de_pc2-ds-wrapper\bin\win`

    with `PC2DedicatedServerWrapper.exe`

    or

    **Linux**

    `C:\_GAMES\Steam\steamapps\common\Project CARS 2 - Dedicated Server\gef-gaming.de_pc2-ds-wrapper\bin\lnx`

    with `PC2DedicatedServerWrapper`


---

## **How to use / Multiple Configurations**

1. In the configs folder:

    `C:\_GAMES\Steam\steamapps\common\Project CARS 2 - Dedicated Server\gef-gaming.de_pc2-ds-wrapper\configs`

    You can create multiple *.ini files like the `basic.ini`

    For example:

    `CUP_R01_Zolder.ini`
    `CUP_R02_LeMans.ini`
    `CUP_R03_Nürburgring.ini`

    Just copy the basic.ini multiple times and edit the names and settings.

2. Start the server with parameters through commandline:

    **Windows**

    `PC2DedicatedServerWrapper.exe CUP_R01_Zolder.ini`

    or

    **Linux**

    `PC2DedicatedServerWrapper CUP_R01_Zolder.ini`


---

## **Additonal Parameters**

`PracticeServer`

Disabling dateprogression, Mandatory Pitstop, license.

Sets weatherprogression to realtime,
practice & quali to 24 hours, race to 1 Lap and password to "".
Useful if you want the same server (under the week, between cup races) for
practice the next track. And without edit your ini files.

`Sunshine`

Overrides all weatherslots with "Clear" and sets all sessions to 1 slot.
Useful if the server is bugging with changing weather. Its the case at the moment i think - 10. March 2018


### You can pass these parameters to the wrapper to override some settings without alter your ini files:

`PC2DedicatedServerWrapper.exe CUP_R01_Zolder.ini PracticeServer`

`PC2DedicatedServerWrapper.exe CUP_R01_Zolder.ini Sunshine`

`PC2DedicatedServerWrapper.exe CUP_R01_Zolder.ini PracticeServer:Sunshine`

**Syntax**

PC2DedicatedServerWrapper.exe ***.ini**(optional) **Parameter**(optional-split by ":")


---


## Startscript Generator

Under

`C:\_GAMES\Steam\steamapps\common\Project CARS 2 - Dedicated Server\gef-gaming.de_pc2-ds-wrapper\bin\win`

you find the

`GenerateStartscripts.exe`


If you execute it, all your ini files in the configs folder are getting a proper startscript under

`C:\_GAMES\Steam\steamapps\common\Project CARS 2 - Dedicated Server\gef-gaming.de_pc2-ds-wrapper\bin\win\startscripts`


### Example on Windows
`CUP_R01_Zolder.bat`

`CUP_R01_Zolder-Practice.bat`

`CUP_R01_Zolder-Sun.bat`

`CUP_R01_Zolder-PracticeSun.bat`

You can then simply start the right .bat file to start the server with the correct .ini file


---


## Known issues & Infos

- **BACKUP YOUR DEDICATED SERVER FILES if you dont want to loose configs etc.! Im not responsible for maybe a dataloss or something! The tool is only tested by me at the moment. Please use it carefully!**
- There are very little errorchecks, so if you make something wrong there is maybe no errormessage or something
- Dont delete or rename the basic.ini
- Of course it can happen that some things dont work. Please report it and i will fix it.
- Simple motd config in ini coming soon
- You must place  the tool/folder in the right position like in the tutorial. If you dont make it correct it cant be started and can maybe cause errors or bugs
- At the moment all variables/values must be in the ini files. If you delete some of them for readability it is not working
. Maybe there are some values case sensitive in the ini at the moment. Be Careful and read the comments above the settings.
- GUI is maybe coming
- Linux support is coming soon
- Feel free to edit the source, im not a python expert. The code is quite messy and repetetive.

## Repository

[https://bitbucket.org/david-maus/gef-gaming.de_pc2-ds-wrapper/src](https://bitbucket.org/david-maus/gef-gaming.de_pc2-ds-wrapper/src)
