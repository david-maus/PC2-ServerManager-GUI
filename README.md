# **Project Cars 2 Server Manager GUI**
[GEF-GAMING.DE](http://www.gef-gaming.de)
---
![alt text](https://i.imgur.com/ly1uVwv.jpg)
## **Server starter / Weather randomizer / Multiple Configs**

*** ------Linux support coming soon / Video & Pictured tutorial coming soon------***

Text Coming Soon

---

## **Features**

- Multiple Config-Files for infinite server/session setups
- MaxGrid / MaxPlayers automatic to max possible for a track
- All possible Tracks and Classes in dropdownboxes
- Easy Setup and no config editing
- Easier Multiclass setup
- Classmode to deactivate the class restriction (All cars possible, for Trackday / Tourist servers)

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


- **Automatic file copy to serverdirectory on start**
 - On every serverstart get the correct and fresh server.cfg / rotateFile / motd / baseFile / statsConfig
 - For use with simresults or other services, the current stats data is deleted before every start
 - For use with simresults or other services, the sessionTracking is activated before every start
 - Edited motd (No WeatherSlots Info in Lobbychat)

---
### ** Thanks to [MortICi](http://forum.projectcarsgame.com/member.php?3295-MortICi) for the sms_base.lua / sms_motd.lua Files and his work on the dedicated server configs!**
[His awesome Thread for the dedicated server configs](http://forum.projectcarsgame.com/showthread.php?56669-Dedicated-Server-Configuration-Sample-Weather-MultiClass-REALLY-FIXED!-2-25-18)

---

## **How to install**

1. Download the Server Manager [here](https://github.com/david-maus/PC2-ServerManager-GUI/archive/master.zip)
2. Extract it anywhere

---

## **How to use**

1. Start the Program
2. Choose a Path to an empty Folder for your servers
3. Click on Login and input at least your Steam Username
4. Input a name for your Server
5. Click on Add Server

Switch / Change / Duplicate / Save your Serversettings and start the Server

---


## Known issues & Infos

- Serverrestart is not tested with the gui and maybe not working!
- You can input your Steam Password in the login window, it will be stored in /data/settings.ini in an unreadable format. It is not a perfect protection but better then nothing. Sadly you must login with your steamaccount to download the dedicated server. Anonymous is not working

- On Add or Update Server the gui is downloading the Official Project Cars 2 Dedicated Server and my [CMD-tools](https://github.com/david-maus/PC2-ServerManager-CMDtool) in order to work correctly.
- There are very little errorchecks, so if you make something wrong there is maybe no errormessage
- Of course it can happen that some things dont work. Please report it and i will fix it.
- Linux support is coming soon
- Feel free to edit the source, im not a python expert. The code is quite messy and repetetive.

## Repository

[https://github.com/david-maus/PC2-ServerManager-GUI](https://github.com/david-maus/PC2-ServerManager-GUI)
