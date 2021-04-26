# win10-terminal-setup
## About
This repository is all about the NEW Windows Terminal APP and what it offers you.  With the new APP you can install multiple shells and access them all in one convenient place.  It will also guide you on customizing a few shells to give you a more visual experience.

> ### What this repo covers (currently still being worked on)
> - Install Terminal APP from scratch
>   - add a theme to give it a personal look (Optional)
> - Install other shells (highly recommended)
> - Custom Configuration
> - Hints and tips to help you out
> - Give links to reference sources

So take advantage of the new .github table of contents to navigate this document.  You can find it located to the left of the README.md file name.

## Prerequisites

1. Time and patience
2. Terminal APP
3. Font (Optional but highly recommended)

> 2. You will need to get the official [Windows Terminal][windowsterminal] APP.  Once the APP is installed it will give you the best terminal experience on Windows.  And allow you to keep adding features to it.  There are multiple ways of acquiring the Windows Terminal.  However the best is from the Microsoft [Store](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701).  This will automatically keep the APP updated for you. 

> 3. Also to get the most out of the customized theme you will need to install a special font.  [Cascadi-Code](https://github.com/microsoft/cascadia-code) is going to be a good place to start.  Click on the name to go to the repo.  Next look on the right side colum and click the latest Release.  Once that opens you will find that there is a zipped file with the font on this page to download.

> NuGet provider is also going to be required but you will be prompted to install this.

> Untrusted repository
> InstallationPolicy value by running the Set-PSRepository cmdlet.

## Installation of custom settings for powershell

Verify the Prerequisites have been met from the section above.

You will need to use the [PowerShell Gallery][powershell-gallery] to install [posh-git][posh-git] and [oh-my-posh][oh-my-posh]:

```powershell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

View the default themes for oh-my-posh and pick one or load my custom theme:

```powershell
# Clear the terminal window so you can scroll back and view all the themes easier.
clear
# The next line will display all the themes installed.  Scroll threw them and pick the theme you want to use and copy it's name.
Get-PoshThemes
# Use this line to set the theme that you picked by replacing {theme-name} with name you copied.
Set-Theme {theme-name}
```


Append the following lines to your PowerShell profile to automatically load on startup:

PowerShell 7 or Pwsh Settings are found using this pathway:
%username%\Documents\PowerShell and then edit the Microsoft.PowerShell_profile.ps1 file as shown below.

```powershell
Import-Module posh-git
Import-Module oh-my-posh
Set-Theme {theme-name}
```

## Configuration

Install custom themes for PowerShell 7 or Pwsh by adding them to theme directory.
This pathway changes with the version of oh-my-posh you are using.
Current oh-my-posh is:  [![GitHub release](https://img.shields.io/github/release/JanDeDobbeleer/oh-my-posh.svg)](https://github.com/JanDeDobbeleer/oh-my-posh/releases/)

Pathway is: %username%\Documents\PowerShell\Modules\oh-my-posh\ {version} \themes




My custom theme red-chaos-line is included in this repo.

## Hints and tips

  Touch is one command you **CAN NOT** use in PowerShell use **'NewItem'** instead
## More Information

Official oh-my-posh links

[![oh-my-posh-repo]][JanDeDobbeleer]
[![Documentation][docs-badge]][docs]


[powershell-gallery]: https://www.powershellgallery.com/
[posh-git]: https://www.powershellgallery.com/packages/posh-git/1.0.0
[oh-my-posh]: https://www.powershellgallery.com/packages/oh-my-posh/3.120.0


[oh-my-posh-repo]: https://img.shields.io/badge/repo-oh--my--posh-blue
[JanDeDobbeleer]: https://github.com/JanDeDobbeleer/oh-my-posh
[docs-badge]: https://img.shields.io/badge/documentation-ohmyposh.dev-blue
[docs]: https://ohmyposh.dev/docs