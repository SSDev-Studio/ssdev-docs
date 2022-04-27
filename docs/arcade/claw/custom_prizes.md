---
sidebar_position: 2
title: Custom Prizes
---

## What is it?
You may want different claw machines across your server to contain different prizes. This is easily achievable with this script!

:::tip
Its best if you simply copy the `defaultPrizes` table in the `config.lua` file and paste it below with a different variable name.
:::

```lua title=config.lua
~~~
local myCustomPrizes = {
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
}
~~~
```

In the above codeblock you can set new prizes for the claw machine. You can even change the model name, the bone to use, the offset, the win rate and the reward.

Back in the config, you need to goto the machine you want to change the prizes for. Once you found it, simply change the "Prizes" table to the one you just created.
```lua
["eclipse"] = {
    MachineModel = 'ch_prop_arcade_claw_01a',
    Distance = 2.5,
    Position = vector3(-803.12, 234.41, 75.68),
    Heading = 359.28,
    ClawMoveSpeed = 0.005,
    Prizes = myCustomPrizes, -- RIGHT HERE
    Price = {
        Type = 'Currency',
        Currency = 'cash',
        Amount = 1000,
    },
    Currency = 'cash',
    DeletePrizeOnWin = false,
    Networked = false
}
```

Thats it! You have changed the prizes in a specific claw machine!

:::tip
You should always backup your config before making changes.
:::