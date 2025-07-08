---
sidebar_position: 7
---

# Advanced Setup

## FNM

If you work on multiple projects, that use different versions of Node, especially for older or legacy projects, you will likely need a version manager for Node. There used to be one fo Windows called Node Version Manager (nvm) but it is being replaced with a new project. So I recommend Fast Node Manager (fnm), instead. The original [NVM](https://github.com/nvm-sh/nvm) for Linux is still excellent.

[Fast Node Manager](https://github.com/Schniz/fnm) works on Linux and Windows and is relatively easy to install, but harder than vanilla Node.js. I highley recommend it if you're on Windows.

### Note on installation

If you are just setting your computer up, and haven't messed with PowerShell, you will likely need to do the PowerShell steps in a certain order.

1. `if (-not (Test-Path $profile)) { New-Item $profile -Force }`
2. `Invoke-Item $profile`
3. Then add this to the end of the file you just opened (might be empty at first) - `fnm env --use-on-cd --shell powershell | Out-String | Invoke-Expression`