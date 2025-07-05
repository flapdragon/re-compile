---
sidebar_position: 5
---

# PowerShell

## What is PowerShell?

[PowerShell](https://learn.microsoft.com/en-us/powershell/scripting/overview?view=powershell-7.5) is a cross-platform task automation solution made up of a command-line shell, a scripting language, and a configuration management framework. PowerShell runs on Windows, Linux, and macOS.

Why you would ever run this on Linux is beyond me.

On Windows, however, it is the most powerful terminal or shell. Command Prompt is great, but PowerShell is more powerful and the terminal of choice for Windows stuff.

## "Execution of scripts is disabled on this system"

The first time you try to run an npm command such as `npm install`, you might get the following warning:

```PowerShell
"Execution of scripts is disabled on this system"
```

This is because, by default, for security reasons, PowerShell disables running scripts, such as npm scripts. That's definitely a good thing, but we need to run scripts, so all we have to do is tell PowerShell that we're cool and to let us run scripts.

## Solution

Open PowerShell as an administrator by hitting the Windows key, then typing `Windows PowerShell` and when it shows up in the results right clicking on it and choosing `Run as administrator`. Inside that PowerShell type:

```PowerShell
Set-ExecutionPolicy RemoteSigned
```

Then close that PowerShell window. Just to be safe you should close all terminal windows before trying to run scripts again.

Stack Overflow has a [famous answer](https://stackoverflow.com/questions/4037939/powershell-says-execution-of-scripts-is-disabled-on-this-system) for this issue. The first answer works best.
