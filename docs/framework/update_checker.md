---
title: Update Checker
sidebar_position: 3
---

## What is it?
This resource has the ability to check for updates for all other SSDev Resources.
By default this functionality is enabled but can be disabled in the `config.lua` file.

:::tip
```lua title=config.lua
Config = {
    DeveloperMode = false,
    UpdateChecking = {
        Enabled = false,
        UpdateServer = "https://api.k8s.ssdev.studio", -- Don't change this
    }
}
```
This disables update checking
:::

:::danger
Disabling update checking is not recommended. If an update is released that fixes a vulnerability, you are less likely to find out about the fix!
:::

## What does it do?
SSDev resources has the ability to use an export called `CheckForUpdates(resourceName)`. It will contact the Update Server and request for the latest updates for the resource.
It then compares the latest version to the version currently installed. If there is a newer version it will notify you in the console on SSDev Framework Startup.