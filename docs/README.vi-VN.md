[English](/README.md) | Tiếng Việt
<div align="center"><h1>Cách làm Terminal Cute</h1></div>

<div align="center">
<h3>Muốn Terminal của bạn cũng cute như thế này? Bạn đến đúng chỗ r á :3!</h3>
</div>

<div align="center">
  <img src="/images/cute.png">
</div>

	
## Setup
### ⚡ Yêu Cầu
- Bạn sẽ cần tải xuống [Terminal từ Microsoft Store](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701).
- Tải xuống và cài đặt [Nerd Fonts](https://www.nerdfonts.com/).
- Tải xuống và cài đặt [App Installer](https://apps.microsoft.com/store/detail/app-installer/9NBLGGH4NNS1) để có thể sử dụng lệnh `winget`.
- Tải xuống [Scoop](https://scoop.sh/).
	
### ⬇️ Cài Đặt
Copy và chạy từng dòng một trong Terminal.

> Tùy chọn: Cần thiết để chạy tập lệnh từ xa lần đầu tiên
```ps1
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
> Cài đặt Scoop
```ps1
irm get.scoop.sh | iex
```
> Cài đặt git nếu bạn chưa có
```ps1
scoop install git
```

## 💻 Windows Terminal Settings
Đặt profile mặc định là **Windows PowerShell**
```
Settings > Default profile > Windows PowerShell
```
Chỉnh sửa một số cài đặt phù hợp với bạn và chọn Font chữ là [CaskaydiaCove NF](/fonts/CascadiaCode.zip) (**CaskaydiaCove NF** hiện không hiển thị đúng biểu tượng ở một số giao diện nên hãy sử dụng [FiraCode Nerd Font](/fonts/FiraCode.zip) thay thế) một số font chữ khác có thể không hiển thị biểu tượng một cách chính xác.

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/02105207-53f3-4a26-b6c4-b33775c53769

Thêm Bảng phối màu cho Terminal, chọn những cái bạn thích trong [Windows Terminal Themes](https://windowsterminalthemes.dev/) và dán chúng vào `settings.json`.

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/de727f8c-d5a1-4819-8d61-861dfef301ef

## 📦 [Cài đặt Oh My Posh](https://ohmyposh.dev/docs/installation/windows)
**Oh My Posh** là một công cụ chủ đề nhanh chóng cho phép làm đẹp chuỗi nhanh chóng. Vui lòng đảm bảo rằng bạn đã làm theo các hướng dẫn trước đó một cách chính xác vì công cụ này cần Terminal của bạn sử dụng **Nerd Font**.
> Mở PowerShell và chạy lệnh sau:
```ps1
winget install JanDeDobbeleer.OhMyPosh -s winget
```
> Dùng khi theme Oh My Posh của bạn đã lỗi thời.
```ps1
winget upgrade JanDeDobbeleer.OhMyPosh -s winget
```
Bây giờ hãy đóng Terminal và mở lại.

> Hãy bắt đầu với theme mặc định:
```ps1
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\jandedobbeleer.omp.json"
```
Chạy lệnh và copy lệnh nó hiện lên và chạy tiếp.

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/f967091f-3e82-4ff8-b68d-d2914e2ef2ff

> Bây giờ hãy chọn chủ đề của bạn:
```ps1
Get-PoshThemes
```
> Chọn chủ đề của bạn và chạy lệnh:
```ps1
oh-my-posh --init --shell pwsh --config <path-to-your-theme>
```
> Lệnh sẽ giống như thế này:
```ps1
oh-my-posh init pwsh --config ~AppData\Local\Programs\oh-my-posh\themes\{theme-name}.omp.json | Invoke-Expression
```

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/eff7ebff-a085-42c5-a08c-b85e84bfe833

Do khi mở một cửa sổ Terminal mới sẽ không có theme **Oh My Posh** nên chúng ta sẽ cấu hình PowerShell profile script để mỗi khi bật Terminal lên nó sẽ tự động sử dụng theme mà chúng ta đã chọn.
> Lệnh khởi tạo profile:
```ps1
New-Item -Path $PROFILE -Type File -Force
```
> Mở profile script bằng Notepad. Sao chép lệnh bạn đã sử dụng để khởi tạo theme trước đó. Dán lệnh vào profile script file và lưu nó.

```ps1
notepad $PROFILE
```

https://github.com/MiyagawaMizu/Cute-Terminal/assets/71164002/1e137776-8d37-4f04-8d6e-cf4504349ef4

> Sau khi thêm, hãy chạy lệnh dưới reload lại theme của bạn để các thay đổi có hiệu lực:
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
