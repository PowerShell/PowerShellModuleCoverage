# PowerShell Module Coverage

> _NOTE_ To report problems with modules that ship in Windows, use the Windows Feedback Hub.
> For more information, see [Send feedback to Microsoft with the Feedback Hub app](https://support.microsoft.com/windows/send-feedback-to-microsoft-with-the-feedback-hub-app-f59187f8-8739-22d6-ba93-f66612949332).

## Windows PowerShell modules with PowerShell Core 6.1

Starting with [Windows 10 Insiders Build 17711](https://blogs.windows.com/windowsexperience/2018/07/06/announcing-windows-10-insider-preview-build-17711/), changes have been made to inbox Windows PowerShell modules to add compatibility with PowerShell Core 6.
With the [Preview.4 release of PowerShell Core 6.1](https://github.com/PowerShell/PowerShell/releases/tag/v6.1.0-preview.4) you can use some Windows PowerShell modules without additional work.

```powershell
Get-Module -ListAvailable

# shows modules from:
#   - $env:UserProfile\Documents\PowerShell\Modules
#   - $env:ProgramFiles\PowerShell\Modules
#   - $env:WinDir\System32\WindowsPowerShell\v1.0\Modules
```

Specifically, modules that have some level of validation will have the `CompatiblePSEditions` property in its module manifest include `Core` which enables it to show up automatically.
Over time, we expect many more inbox Windows PowerShell modules to be converted to be compatible and have their `CompatiblePSEditions` property updated.

## Issues with Windows PowerShell modules on PowerShell Core

This repo is for the purpose of tracking user found issues where a module is not working as expected compared to Windows PowerShell 5.1.
Even with modules that are marked as compatible with PowerShell Core 6.1,
you may find some issues that were not discovered as part of our validation.
Please see if an existing issue exists in this repo 
and give it a 👍 to vote up its priority.
If no issue exists, please open one so that we know about it.
