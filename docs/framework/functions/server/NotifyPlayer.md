Used to notify the player from the server side

## Parameters
| Name | Parameter |
| --- | --- |
| source | The source of the player |
| title | Title of the notification |
| message | Message of the notification |
| color | Color of the notification |
| icon | Icon of the notification |

## Return Type
Void

## Invoke
```lua
local framework = exports["ssdev_framework"]:GetFramework()
framework:NotifyPlayer(source, title, message, color, icon)
```

## Example
```lua
local framework = exports["ssdev_framework"]:GetFramework()
framework:NotifyPlayer(1, "Title", "Message", "red", "fa fas-award")
```

:::note Bare in mind
The additional parameters may not be used depending on your framework.
:::
