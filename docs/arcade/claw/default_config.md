---
sidebar_position: 1
title: Default Config
---

```lua title=config.lua
-- WinRate = If the value is 20, each game there is a 20% chance of winning the prize. 100 means always winnable. 0 means never winnable. When the prize is not winnable the claw will fail to pickup the prize

local defaultPrizes = {
    ['ch_prop_arcade_claw_plush_02a'] = { -- Left Back
        PickupBone = 2,
        offset = vector3(leftSidePrizeX, backPrizeY, defaultZOffsetFloor),
        WinRate = 20,
        Reward = {
            Type = 'Currency',
            Currency = 'cash',
            Amount = 1000,
        }
    },
    ['ch_prop_arcade_claw_plush_03a'] = { -- Left Center
        PickupBone = 2,
        offset = vector3(leftSidePrizeX, centerPrizeY, defaultZOffsetFloor),
        WinRate = 30,
        Reward = {
            Type = 'Currency',
            Currency = 'cash',
            Amount = 1000,
        }
    },
    ['ch_prop_arcade_claw_plush_04a'] = { -- Center Back
        PickupBone = 2,
        offset = vector3(centerSidePrizeX, backPrizeY, defaultZOffsetFloor),
        WinRate = 40,
        Reward = {
            Type = 'Currency',
            Currency = 'cash',
            Amount = 1000,
        }
    },
    ['ch_prop_arcade_claw_plush_05a'] = { -- Center Center
        PickupBone = 2,
        offset = vector3(centerSidePrizeX, centerPrizeY, defaultZOffsetFloor),
        WinRate = 70,
        Reward = {
            Type = 'Currency',
            Currency = 'cash',
            Amount = 1000,
        }
    },
    ['ch_prop_arcade_claw_plush_06a'] = { -- Center Front
        PickupBone = 0,
        offset = vector3(centerSidePrizeX, frontPrizeY, defaultZOffsetFloor),
        WinRate = 100,
        Reward = {
            Type = 'Event',
            Event = 'ssdev_arcade_claw:ExampleWinEvent',
        }
    },
    ['ch_prop_princess_robo_plush_07a'] = { -- Right Back
        PickupBone = 2,
        offset = vector3(rightSidePrizeX, backPrizeY, defaultZOffsetFloor),
        WinRate = 80,
        Reward = {
            Type = 'Item',
            Item = 'sandwich',
            Amount = 10,
        }
    },
    ['ch_prop_shiny_wasabi_plush_08a'] = { -- Right Center
        PickupBone = 2,
        offset = vector3(rightSidePrizeX, centerPrizeY, defaultZOffsetFloor),
        WinRate = 15,
        Reward = {
            Type = 'Item',
            Item = 'sandwich',
            Amount = 10,
        }
    },
    ['ch_prop_master_09a'] = { -- Right Front
        PickupBone = 2,
        offset = vector3(rightSidePrizeX, frontPrizeY, defaultZOffsetFloor),
        WinRate = 5,
        Reward = {
            Type = 'Item',
            Item = 'sandwich',
            Amount = 10,
        }
    }
}

Config = {
    LoggingLevel = 3, -- 0 = Errors, 1 = Warnings, 2 = Info, 3 = Debug, 4 = Trace
    TargettingMode = 'QBTarget', -- Distance | Command | QBTarget | QTarget
    Machines = {
        ["legion"] = { -- Name of the machine
            MachineModel = 'ch_prop_arcade_claw_01a', -- This is the only model in GTA. If you stream custom claw machine models, change it here.
            Distance = 2.5, -- Distance you have to be from the machine to be able to use it.
            Position = vector3(207.6, -919.66, 30.69), -- The position of the machine.
            Heading = 229.95, -- The heading of the machine.
            ClawMoveSpeed = 0.005, -- The speed of the claw. Increase = faster | Decrease = slower
            Prizes = defaultPrizes, -- Prizes this machine contains
            Price = {
                Type = 'Currency', -- Currency/Item
                Currency = 'cash', -- Currency name/Item name
                Amount = 1000, -- Amount to take from player
            },
            DeletePrizeOnWin = false, -- True = Will delete the entity when won | False = Will teleport the entity back to its starting position
            Networked = false  -- [Placeholder for future update] True = machine, claw and prizes will be networked. (This is not recommended as when entities move they are jittery) | False = machine, claw and prizes will be local (Players will not see what other players see)
        },
        ["eclipse"] = {
            MachineModel = 'ch_prop_arcade_claw_01a',
            Distance = 2.5,
            Position = vector3(-803.12, 234.41, 75.68),
            Heading = 359.28,
            ClawMoveSpeed = 0.005,
            Prizes = defaultPrizes,
            Price = {
                Type = 'Currency',
                Currency = 'cash',
                Amount = 1000,
            },
            Currency = 'cash',
            DeletePrizeOnWin = false,
            Networked = false
        }
    }
}

Logger = exports["ssdev_framework"]:GetLogger(GetCurrentResourceName(), Config.LoggingLevel)
Framework = exports["ssdev_framework"]:GetFramework()
```