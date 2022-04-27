---
sidebar_position: 3
title: Custom Win Events
---

## What are win events?
These are events that are called when a player wins a prize from the claw machine.

In the config for the specific prize you will need to set the event that will be called when the player wins.

```lua title=config.lua
~~~~
['ch_prop_arcade_claw_plush_06a'] = { -- Center Front
        PickupBone = 0,
        offset = vector3(centerSidePrizeX, frontPrizeY, defaultZOffsetFloor),
        WinRate = 100,
        Reward = {
            Type = 'Event',
            Event = 'ssdev_arcade_claw:ExampleWinEvent',
        }
    },
~~~~
```

You are mainly needing to look at the Reward section in the codeblock above. You will need to change the Type to "Event" and then change the "Event" to the name of the event you want to call.


## Example Event
This is the example event that is called when a player wins the prize. It is ONLY called when the player legitimately wins the prize, it will not be called if the player cheated the game.
```lua
AddEventHandler('ssdev_arcade_claw:ExampleWinEvent', function (source, game, prizeName)
    local machine = Config.Machines[game.MachineName]
    local reward = machine.Prizes[prizeName].Reward
    Logger:Debug(source .. " just won " .. prizeName .. " from " .. game.MachineName .. " with reward " .. reward.Type)
end)
```