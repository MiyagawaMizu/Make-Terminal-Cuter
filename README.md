<div align="center"><h1>Cute-Terminal</h1></div>

<div align="center">
Want to make a cute terminal like this, show it off to your non-IT friends? Well, you've come to the right place!
</div>

<div align="center">
  <img src="/images/cute.png">
</div>

	
## Setup
### ⚡ Requirements
- You will need to download [Terminal from the Microsoft Store](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701).
- Download and install [Nerd Fonts](https://www.nerdfonts.com/).
- Download and install [App Installer](https://apps.microsoft.com/store/detail/app-installer/9NBLGGH4NNS1) to use `winget` commands.
- Install [Scoop](https://scoop.sh/).

	
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

### 💻 Windows Terminal Settings
Adjust some settings to suit you and choose Font face to [CaskaydiaCove NF](/fonts/CascadiaCode.zip) or [FiraCode Nerd Font](/fonts/FiraCode.zip) other fonts may not render icons properly.

https://github.com/MiyagawaMizu/Cute-Terminal/blob/main/videos/nerd_fonts.mp4

Add a Color Scheme for Terminal, select the ones you like in [Windows Terminal Themes](https://windowsterminalthemes.dev/) and paste them in `settings.json`.

[](/videos/color_scheme.mp4)

### 📦 [Install Oh My Posh](https://ohmyposh.dev/docs/installation/windows)
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

[](/videos/default_theme.mp4)

> Now let's pick your theme:
```ps1