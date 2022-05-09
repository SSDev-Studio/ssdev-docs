Check if the player has the item in his inventory

## Parameters
| Name | Parameter |
| --- | --- |
| source | The source of the player |
| item | Item name |
| amount | Amount of the item to check for |

## Return Type
Boolean

## Invoke
```lua
local framework = exports["ssdev_framework"]:GetFramework()
framework:CheckInventoryForItem(source, item, amount)
```

## Example
```lua
local framework = exports["ssdev_framework"]:GetFramework()
local hasItem = framework:CheckInventoryForItem(1, "sandwich", 1)
print("Player has 1 sandwich: " .. tostring(hasItem))
```

:::note Bare in mind
The additional parameters may not be used depending on your framework.
:::
