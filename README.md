<div align="center">

# ✨ NixOS Dotfiles ✨

![Main Screenshot](screenshot/logo.png)

> _A beautiful NixOS configuration with Hyprland_

[![NixOS](https://img.shields.io/badge/NixOS-Unstable-blue.svg?style=flat-square&logo=nixos&logoColor=white)](https://nixos.org)
[![Hyprland](https://img.shields.io/badge/Hyprland-dynamic-blue.svg?style=flat-square)](https://hyprland.org)
[![License](https://img.shields.io/badge/license-MIT-orange.svg?style=flat-square)](LICENSE)

[Screenshots](#-screenshots) • [Features](#-features) •
[Installation](#-installation) • [Keybindings](#-keybindings)

</div>

---

## 📸 Screenshots

<div align="center">

|    NVF & Workspace     |    Rofi & Terminal     |
| :--------------------: | :--------------------: |
| ![1](screenshot/1.png) | ![2](screenshot/2.png) |
| ![3](screenshot/3.png) | ![4](screenshot/4.png) |

</div>

---

## 🎯 Features

### 🖥️ Core Components

<table align="center">
<tr>
<td width="50%">

**🪟 Window Manager & UI**

- **Hyprland** - Wayland compositor
- **Waybar** - Status bar
- **Rofi** - Application launcher
- **Swww** - Wallpaper daemon
- **Pywal** - Dynamic theming

</td>
<td width="50%">

**💻 Terminal & Shell**

- **Kitty** - GPU accelerated terminal
- **Fish** - Friendly shell
- **Zoxide** - Smart directory jumper
- **FastFetch** - System info
- **BTop** - System monitor

</td>
</tr>
<tr>
<td width="50%">

**🛠️ Development**

- **Vim/NVim** - Text editors
- **NVF** - Neovim IDE
- **Git** - Version control
- **LSD** - Modern ls alternative

</td>
<td width="50%">

**🎨 Applications**

- **Zen Browser** - Web browser
- **Nemo** - File manager
- **GIMP** - Image editor
- **MPV** - Media player
- **Telegram** - Messenger

</td>
</tr>
</table>

---

## ⌨️ Keybindings

<div align="center">

|          Keybind          |     Action      |          Keybind          |      Action      |
| :-----------------------: | :-------------: | :-----------------------: | :--------------: |
|     `SUPER + RETURN`      |  Open Terminal  |        `SUPER + Q`        |   Kill Window    |
|        `SUPER + R`        |  App Launcher   |        `SUPER + F`        |    Fullscreen    |
|        `SUPER + E`        |  File Manager   |        `SUPER + W`        |   Web Browser    |
|      `CTRL + SPACE`       | Switch Language |     `ALT + SHIFT + S`     |    Screenshot    |
|    `SUPER + SHIFT + D`    |    Telegram     |    `SUPER + SHIFT + W`    |      Steam       |
|    `SUPER + SHIFT + E`    |      GIMP       |   `CTRL + SHIFT + 1-0`    | Change Wallpaper |
| `SUPER + SHIFT + ALT + S` |      Sleep      | `SUPER + SHIFT + ALT + Q` |    Power Off     |

</div>

---

## 🔧 Shell Aliases

<div align="center">

|   Alias   |                       Command                        |   Alias   |            Command            |
| :-------: | :--------------------------------------------------: | :-------: | :---------------------------: |
|   `ll`    |                      `lsd -lah`                      |   `la`    |           `lsd -a`            |
|   `ls`    |                        `lsd`                         |   `..`    |            `cd ..`            |
|   `...`   |                      `cd ../..`                      |  `grep`   |      `grep --color=auto`      |
|   `nvf`   |            `nix run github:notashelf/nvf`            |  `snvf`   |          `sudo nvf`           |
|   `gs`    |                     `git status`                     |   `ga`    |           `git add`           |
|   `gc`    |                     `git commit`                     |   `gp`    |          `git push`           |
|   `gcl`   |                     `git clone`                      |  `gpam`   |    `git push origin main`     |
| `rebuild` | `sudo nixos-rebuild switch --flake /etc/nixos#nixos` | `cleanup` | `sudo nix-collect-garbage -d` |

</div>

---

## 📦 Installation

### Prerequisites

- Fresh NixOS installation
- Username set to `nixos` (recommended)

### 🚀 Quick Start

```bash
# 1️⃣ Install git (RECOMMENDED)
sudo nano /etc/nixos/configuration.nix
# Add: environment.systemPackages = with pkgs; [ git ];
sudo nixos-rebuild switch

# 2️⃣ Clone repository
git clone https://github.com/ass-sudo/nix-dotfiles.git
cd nix-dotfiles/nixos

# 3️⃣ Backup and copy files (RECOMMENDED)
sudo rm -rf /etc/nixos/configuration.nix
sudo cp -a configuration.nix dotfiles/ flake.lock flake.nix home/ modules/ /etc/nixos/

# 4️⃣ Apply configuration
sudo nixos-rebuild switch --flake /etc/nixos#nixos
reboot
```

---

## ⚙️ Configuration

### 🖥️ Display Settings

Edit your monitor configuration:

```bash
nano ~/.config/hypr/hyprland.conf
```

```conf
# Example configuration
monitor = DP-1, 1920x1080@165, 0x0, 1
```

### ⚠️ Important Notes

- **Use user name** nixos
- **Do not change** the layout switch from `ALT + SHIFT` as it may break
  bindings
- Adjust monitor settings according to your hardware
- For multiple monitors, add additional `monitor` lines

---

## 🤝 Contributing

Contributions are welcome! Feel free to:

- 🐛 Report bugs
- 💡 Suggest new features
- 🔧 Submit pull requests

---

<div align="center">

### ⭐ Star this repo if you find it helpful!

Made with by [ass-sudo](https://github.com/ass-sudo)

</div>
