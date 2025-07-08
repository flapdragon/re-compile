---
sidebar_position: 7
---

# Advanced Setup

## FNM

If you work on multiple projects, that use different versions of Node, especially for older or legacy projects, you will likely need a version manager for Node. There used to be one for Windows called [Node Version Manager (nvm)](https://github.com/coreybutler/nvm-windows?tab=readme-ov-file) but it is being replaced with a new project called [Runtime](https://github.com/coreybutler/nvm-windows/wiki/Runtime). The original [NVM](https://github.com/nvm-sh/nvm) for Linux is still excellent.

On Windows, I highly recommened [Fast Node Manager (fnm)](https://github.com/Schniz/fnm) which also works on Linux and is relatively easy to install, but harder than vanilla Node.js. It is my favorite on Windows.

### Note on installation

If you are just setting your computer up, and haven't messed with PowerShell, you will likely need to do the PowerShell steps in a certain order. Just clarifying the [steps from fnm](https://github.com/Schniz/fnm?tab=readme-ov-file#powershell):

1. `if (-not (Test-Path $profile)) { New-Item $profile -Force }`
2. `Invoke-Item $profile`
3. Then add this to the end of the file you just opened (might be empty at first) - `fnm env --use-on-cd --shell powershell | Out-String | Invoke-Expression`