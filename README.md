# Windows PowerShell modules with PowerShell Core 6.1

Starting with [Windows 10 Insiders Build 17711](https://insider.windows.com/en-us/), changes have been made to inbox Windows PowerShell modules to add compatibility with PowerShell Core 6.
With the [Preview.4 release of PowerShell Core 6.1](https://github.com/PowerShell/PowerShell/releases/tag/v6.1.0-preview.4) you can use some Windows PowerShell modules without additional work.

```powershell
Get-Module -ListAvailable

# shows modules from:
#   - $env:UserProfile\Documents\PowerShell\Modules
#   - $env:ProgramFiles\PowerShell\Modules
#   - $env:WinDir\System32\WindowsPowerShell\v1.0\Modules
```

Specifically, modules that have some level of validation will have the `CompatiblePSEditions` property in its module manifest include `Core` which enables it to show up automatically.
Over time, we expect many more inbox Windows PowerShell modules to be converted to be compatible and have its `CompatiblePSEditions` property updated.

# Issues with inbox Windows PowerShell modules

This repo is for the purpose of tracking user found issues where a module is not working as expected compared to Windows PowerShell 5.1.
Although we tried to perform some validation, we have not exhaustively tested everything with PowerShell Core 6.1 so we expect there may be some issues found at runtime that were not discovered at build time.
Please see if an existing issue exists in this repo, if so, you can give it a `thumbs up` to vote it higher in priority.  Or if no issue exists, please open a new issue.
