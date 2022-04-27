---
sidebar_position: 1
title: Events
---

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