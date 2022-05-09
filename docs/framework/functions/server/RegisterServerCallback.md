Used to create server callbacks.

## Parameters
| Name | Parameter |
| --- | --- |
| name | The name of the callback (to be used from the client to invoke this callback) |
| cb | A function reference to execute when this callback is invoked |

## Return Type
Void

## Invoke
```lua
local framework = exports["ssdev_framework"]:GetFramework()
framework:RegisterServerCallback(name, cb)
```

## Example
```lua
local framework = exports["ssdev_framework"]:GetFramework()
framework:RegisterServerCallback("MyServerCallback", function(source, cb, ...)
    print("You have triggered MyServerCallback")
end)
```

Please see the client "TriggerServerCallback" function for more information on executing this callback from the client.