---
title: Logger Utility
sidebar_position: 2
---

## What is it?
This is a utility for logging messages to the console.

:::note Minimum Logging Level
The logging level that you set will determine what messages will be logged into console.
It follows a "Minimum Severity" system. The higher the level the more messages will be logged.
For Example: If you set the logging level to 2, it will log messages that are Errors (0), Warnings (1) and Info (2).
:::

### How to use it
```lua
local logger = exports["ssdev_framework"]:GetLogger("Logger Name", 2)

logger:Info("This is an info message")
logger:Debug("This is a debug message")
logger:Warning("This is a warning message")
logger:Error("This is an error message")
logger:Trace("This is an trace message")
```

:::tip
You can use `GetCurrentResourceName()` in replacement of "Logger Name" to use the invoking resources name.
:::

### Logging Levels
| Level | Description |
|:------|:------------|
| 0 | Error |
| 1 | Warning |
| 2 | Info |
| 3 | Debug |
| 4 | Trace |