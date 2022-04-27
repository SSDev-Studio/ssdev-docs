---
sidebar_position: 1
title: Inside Track
---

![Logo](https://cloud.k8s.alexr03.dev/giRa0/hUJUPIjO78.png/raw.png)

#  SSDev Studio - Inside Track
**SSDev InsideTrack** is an addition to the casino, it allows both **single player** and **multiplayer** horse racing in the "**InsideTrack**" area! 

## Important Links
- [Tebex](https://store.ssdev.studio/package/5047959)
- [Demo](https://cloud.k8s.alexr03.dev/giRa0/rERumAYO74.mp4/raw.mp4)
- [Example Config](https://cloud.k8s.alexr03.dev/giRa0/GEroZAjU71.png/raw.png)

## Dependencies
- **SSDev_Framework** (This allows the use of multiple frameworks. [Github](https://github.com/SSDev-Studio/ssdev_framework)/[Download](https://github.com/SSDev-Studio/ssdev_framework/archive/refs/heads/master.zip))
- **Casino IPL** ([Cayo Perico & Casino DLC IPL Loader](https://forum.cfx.re/t/cayo-perico-casino-dlc-ipl-loader/2099391)) / Or a casino that has the InsideTrack area
- **QTarget** (**Optional**)
- **QBTarget** (**Optional**)
*If you do not use either **QTarget** OR **QBTarget** you will need to access the betting consoles using a command. You also have the option to use your own targetting system using the events below.*

## Features:
- **Optimized**
	- **0.00ms** when not near InsideTrack area
	- **0.02ms - 0.04ms** when near InsideTrack area
	- **0.03ms - 0.05ms** when betting console is open
- Works across multiple frameworks **ESX | QB-Core | Custom (Standalone)**
- Can play single player games while players wait for the multiplayer game to start
- Multiplayer horses synced across all participants screens (Everyone sees the same race, horse positions, horse colours, horse winner)
- **Security**
 	- Ability to add your own ban resource for when players attempt to *cheat/exploit* the game
 	- Horse winners are determined server side instead of client side, unlike other scripts.
 	- Server determines the winning amount to give to the player and the client does not send a custom amount to the server them self.
 	- Protection against:	
		- Betting twice on the same game
		- Betting on a game thats already in progress
		- Betting on a non existent horse
- **Fully Customizable**
	- Ability to open the console using QTarget or a Command
 	- Ability to change the currency that the players play with and win
 	- Rules button can be enabled and disabled
 	- Ability to change the minimum and maximum game duration (Game duration is random between these two values)
 	- Ability to change the amount of time there is between multiplayer games
 	- Ability to change how long the results screen is shown for
 	- Ability to change the default horse name
 	- Ability to automatically set the horse name to the first person who betted on it name.
 	- Changeable horse colours
 	- Minimum and Maximum bet amounts
 	- Bet multiplier for the winnings
 	- Changeable bet increment/decrements amounts
 	- Overridable settings for both single player and multiplayer
 	- Configurable betting console positions
 	- Custom Rules Screen
 	- Custom Scaleform
 	- Locale Support
 	- Currency/Item support
 	- Togglable sound effects

## Updates
### v1.1.0
- [x] Added options for ambient sound in the InsideTrack area.
- [x] Added configurable sound (You can enable/disable the starting sound, the race loop sound, etc)
- [x] Added Item support (You can now configure it to use chips, etc)
- [x] Stream custom scaleform for the inside track.
- [x] You can now configure the inside track rules button to show custom rules (see config)
- [x] Locale Support (You can add your own translations in the Config file)
- [x] Added advanced screen settings in the Config (You can set the render radius, coords, type of screen, etc)
- [x] Added custom horse names (You can define your own list of names in the Config file for the horses instead of using GTA's localised ones)
- [x] Added custom notification icon & title.
- [x] Added custom rules (You can define your own list of rules in the Config file)

##  Available Events
### Client Events
| Event Name | Description |
|--|--|
| ssdev_insidetrack:openConsole | Opens the betting console |
| ssdev_insidetrack:closeConsole | Closes the betting console |

### Server Events
|Event Name| Description |
|--|--|
| ssdev_insidetrack:multiplayer:requestGameData | Calling this will request the multiplayer game state. This is called internally and you do not need to call this yourself. But you can call it to force an update. |

## Screenshots
![Main Betting Screen](https://cloud.k8s.alexr03.dev/giRa0/MoxIbOwo30.jpg/raw.jpg)
![Horses Racing](https://cloud.k8s.alexr03.dev/giRa0/tOFaHeQa03.jpg/raw.jpg)
![Betting screen for main event](https://cloud.k8s.alexr03.dev/giRa0/jOKiLaxO51.jpg/raw.jpg)
![Perf 1](https://cloud.k8s.alexr03.dev/giRa0/HizUteJo40.png/raw.png)
![Perf 2](https://cloud.k8s.alexr03.dev/giRa0/kIZenAGe50.png/raw.png)
![Perf 3](https://cloud.k8s.alexr03.dev/giRa0/BAHIJogU88.jpg/raw.jpg)

|  |  |
|---|---|
| Code is accessible | Semi |
| Subscription-based | No |
| Lines (approximately) | ~1500 |
| Requirements |  READ DEPENDENCIES |
| Support | Yes |