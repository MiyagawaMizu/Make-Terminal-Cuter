	
English | [Tiếng Việt](./docs/README.vi-VN.md)
<div align="center"><h1>How to Make Terminal Cute</h1></div>

<div align="center">
<h3>Want to make a cute terminal like this? You've come to the right place UwU!</h3>
</div>

<div align="center">
  <img src="/images/cute.png">
</div>

	
## Setup
### ⚡ Requirements
- You will need to download [Terminal from the Microsoft Store](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701).
- Download and install [Nerd Fonts](https://www.nerdfonts.com/).
- Download and install [App Installer](https://apps.microsoft.com/store/detail/app-installer/9NBLGGH4NNS1) to use `winget` commands.
- Install [Scoop](https://scoop.sh/) for Neofech and Winfetch Installastion.
	
### ⬇️ Installation
Copy and run the command line by line in Terminal.

> Optional: Needed to run a remote script the first time
```ps1
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
> Install Scoop
```ps1
irm get.scoop.sh | iex
```
> Install git if you haven't already
```ps1
scoop install git
```

## 💻 Windows Terminal Settings
Set Default profile as **Windows PowerShell**
```
Settings > Default profile > Windows PowerShell
```
Adjust some settings to suit you and choose Font face to [CaskaydiaCove NF](/fonts/CascadiaCode.zip) (Sorry **CaskaydiaCove NF** actually broken icons at some theme so use [FiraCode Nerd Font](/fonts/FiraCode.zip) instead) some other fonts may not render icons properly.

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/02105207-53f3-4a26-b6c4-b33775c53769

Add a Color Scheme for Terminal, select the ones you like in [Windows Terminal Themes](https://windowsterminalthemes.dev/) and paste them in `settings.json`.

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/de727f8c-d5a1-4819-8d61-861dfef301ef

## 📦 [Install Oh My Posh](https://ohmyposh.dev/docs/installation/windows)
**Oh My Posh** is a prompt theme engine that enables prompt string beautification. Please ensure that you followed the previous instructions precisely because this engine needs your Terminal to utilize a **Nerd Font**.

> Open a PowerShell prompt and run the following command:
```ps1
winget install JanDeDobbeleer.OhMyPosh -s winget
```
> Used when your Oh My Posh theme is outdated.
```ps1
winget upgrade JanDeDobbeleer.OhMyPosh -s winget
```
Now close Terminal and open it again.

> Let's start with the default theme:
```ps1
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\jandedobbeleer.omp.json"
```
Run the command and copy the command it shows up and continue running.

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/f967091f-3e82-4ff8-b68d-d2914e2ef2ff

> Now let's pick your theme:
```ps1
Get-PoshThemes
```
> Pick your theme and run the command:
```ps1
oh-my-posh --init --shell pwsh --config <path-to-your-theme>
```
> The command should look something like this:
```ps1
oh-my-posh init pwsh --config ~AppData\Local\Programs\oh-my-posh\themes\{theme-name}.omp.json | Invoke-Expression
```

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/eff7ebff-a085-42c5-a08c-b85e84bfe833

Since when opening a new Terminal window it will not have the **Oh My Posh** theme, so we will configure the PowerShell profile script so that every time we turn on Terminal, it will automatically use the theme we have selected.
> Profile initialization command:
```ps1
New-Item -Path $PROFILE -Type File -Force
```
> Open profile script with Notepad. Copy the command you used to initialize the theme earlier. Paste the command into the profile script and save it.

```ps1
notepad $PROFILE
```

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/1e137776-8d37-4f04-8d6e-cf4504349ef4

> Once added, reload your profile for the changes to take effect:
```ps1
. $PROFILE
```

## ⚙️ Install [Neofetch](https://github.com/dylanaraps/neofetch) / [Winfetch](https://github.com/lptstr/winfetch)

Both **Neofetch** and **Winfetch** are command-line system information utilities that display information about your operating system, software, and hardware in an aesthetic and visually pleasing way. But **Winfetch** will be more personalized, so if you want to be fast, you can use Neofetch.
> Install Neofetch
```ps1
scoop install neofetch
```
> Show your system information
```ps1
neofetch
```

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/c1ffd589-99f0-4f44-adff-7c8d98ae7109

> Install Winfetch
```ps1
scoop install winfetch
```
> Setup script
```ps1
Install-Script -Name pwshfetch-test-1
```
Choose “Yes” for any prompts you encountered.
> Restart your Terminal. Then, run winfetch to see if it’s correctly installed.
```ps1
winfetch
```

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/6d595282-5413-4271-b759-4040314c6f01

<!-- If it showing bug like this:

[](/images/winfetch_bug.png)

> Open folder path:
```
"C:\Program Files\WindowsPowerShell\Scripts\pwshfetch-test-1.ps1"
```
> Open the script with any text editor and delete lines that has the error:
```ps1

``` -->

### 🖼️ Custom Image for Winfetch
Because Windows Terminal cannot produce full quality graphics, the Windows logo to the left can be altered to a custom "image" that looks more like a low resolution pixel art.

1. Copy path to your image.
2. Go to this path to edit the config file:
```
C:\Users\{user}\.config\winfetch\config.ps1
```

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/1623ac24-d4de-4186-8181-300454bb0c5a

That's all the steps to make your Terminal more cutie. If you have any questions feel free to contact me (｡•̀ᴗ-)✧.

[![](https://img.shields.io/badge/Discord:%20miyagawamizu-7289DA?logo=discord&logoColor=white)](https://discord.com/users/350945523810959361)
[![](https://img.shields.io/badge/Facebook-1877F2?logo=facebook&logoColor=white)](https://www.facebook.com/miyagawamizu)
[![](https://img.shields.io/badge/Telegram-2ca5e0?logo=telegram&logoColor=white)](https://t.me/miyagawamizu)
