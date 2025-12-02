<div align="center">

# ✨ NixOS Dotfiles ✨

 *A beautiful, modern NixOS configuration with Hyprland*

![Main Setup](screenshot/5.png)

[![NixOS](https://img.shields.io/badge/NixOS-Unstable-blue.svg?style=for-the-badge&logo=nixos&logoColor=white)](https://nixos.org)
[![Hyprland](https://img.shields.io/badge/Hyprland-Wayland-00ADD8.svg?style=for-the-badge&logo=wayland&logoColor=white)](https://hyprland.org)
[![License](https://img.shields.io/badge/License-GNU%20GPL-orange.svg?style=for-the-badge)](LICENSE)

[![Stars](https://img.shields.io/github/stars/ass-sudo/nix-dotfiles?style=social)](https://github.com/ass-sudo/nix-dotfiles/stargazers)
[![Forks](https://img.shields.io/github/forks/ass-sudo/nix-dotfiles?style=social)](https://github.com/ass-sudo/nix-dotfiles/network/members)

[Screenshots](#-screenshots) • [Features](#-features) • [Installation](#-installation) • [Keybindings](#-keybindings) • [Aliases](#-shell-aliases)

---

</div>

## 📸 Screenshots

<div align="center">

| NVF & Workspace | Rofi & Terminal |
|:---------------:|:---------------:|
| ![1](screenshot/1.png) | ![2](screenshot/2.png) |
| ![3](screenshot/3.png) | ![4](screenshot/4.png) |

</div>

---

## 🎯 Features

<div align="center">

### 🖥️ Core Components

</div>

<table align="center">
<tr>
<td width="50%" valign="top">

#### 🪟 Window Manager & UI
- **Hyprland** - Dynamic tiling Wayland compositor
- **Waybar** - Highly customizable status bar
- **Rofi** - Application launcher & window switcher
- **Swww** - Efficient animated wallpaper daemon
- **Pywal** - Automatic color scheme generation

</td>
<td width="50%" valign="top">

#### 💻 Terminal & Shell
- **Kitty** - GPU-accelerated terminal emulator
- **Fish** - Smart and user-friendly shell
- **Zoxide** - Smarter cd command with frecency
- **FastFetch** - Lightning-fast system information
- **BTop** - Resource monitor with modern UI

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 🛠️ Development Tools
- **Vim/NVim** - Powerful text editors
- **NVF** - Neovim IDE with LSP support
- **Git** - Distributed version control
- **LSD** - Modern replacement for ls command

</td>
<td width="50%" valign="top">

#### 🎨 Applications
- **Zen Browser** - Privacy-focused web browser
- **Nemo** - Feature-rich file manager
- **GIMP** - Professional image editor
- **MPV** - Minimalist media player
- **Telegram** - Secure messenger
- **Steam** - Gaming platform

</td>
</tr>
</table>

---

## ⌨️ Keybindings

<div align="center">

| Keybind | Action | Keybind | Action |
|:-------:|:------:|:-------:|:------:|
| `SUPER + RETURN` | Open Terminal | `SUPER + Q` | Kill Window |
| `SUPER + R` | App Launcher | `SUPER + F` | Fullscreen |
| `SUPER + E` | File Manager | `SUPER + W` | Web Browser |
| `CTRL + SPACE` | Switch Language | `ALT + SHIFT + S` | Screenshot |
| `SUPER + SHIFT + D` | Telegram | `SUPER + SHIFT + W` | Steam |
| `SUPER + SHIFT + E` | GIMP | `CTRL + SHIFT + 1-0` | Change Wallpaper |
| `SUPER + SHIFT + ALT + S` | Sleep Mode | `SUPER + SHIFT + ALT + Q` | Power Off |

</div>

---

## 🔧 Shell Aliases

<div align="center">

| Alias | Command | Alias | Command |
|:-----:|:-------:|:-----:|:-------:|
| `ll` | `lsd -lah` | `la` | `lsd -a` |
| `ls` | `lsd` | `..` | `cd ..` |
| `...` | `cd ../..` | `grep` | `grep --color=auto` |
| `nvf` | `nix run github:notashelf/nvf` | `snvf` | `sudo nvf` |
| `gs` | `git status` | `ga` | `git add` |
| `gc` | `git commit` | `gp` | `git push` |
| `gcl` | `git clone` | `gpam` | `git push origin main` |
| `rebuild` | `sudo nixos-rebuild switch --flake /etc/nixos#nixos` | `cleanup` | `sudo nix-collect-garbage -d` |

</div>

---

## 📦 Installation

### Prerequisites
- Fresh NixOS installation
- Username: `nixos` **(recommended)**
- Basic understanding of Nix flakes

### 🚀 Quick Start

```bash
# 1️⃣ Install git (REQUIRED)
sudo nano /etc/nixos/configuration.nix
# Add to systemPackages: git
sudo nixos-rebuild switch

# 2️⃣ Clone this repository
git clone https://github.com/ass-sudo/nix-dotfiles.git
cd nix-dotfiles/nixos

# 3️⃣ Backup and copy configuration files (RECOMMENDED)
sudo rm -rf /etc/nixos/configuration.nix
sudo cp -a configuration.nix dotfiles/ flake.lock flake.nix home/ modules/ /etc/nixos/

# 4️⃣ Apply the configuration
sudo nixos-rebuild switch --flake /etc/nixos#nixos

# 5️⃣ Reboot your system
reboot
```

---

## ⚙️ Configuration

### 🖥️ Display Settings

Configure your monitor in Hyprland:

```bash
nano ~/.config/hypr/hyprland.conf
```

Example configuration:
```conf
monitor = DP-1, 1920x1080@165, 0x0, 1
# For multiple monitors:
# monitor = HDMI-A-1, 1920x1080@60, 1920x0, 1
```

### ⚠️ Important Notes

- ✅ Use username **`nixos`** for best compatibility
- ⚠️ **Do not change** the layout switch from `ALT + SHIFT` (breaks keybindings)
- 📊 Adjust monitor settings according to your hardware
- 🖥️ For multiple monitors, add additional `monitor` lines
- 🎨 Pywal themes are generated automatically from your wallpaper

### 🎨 Customization

- **Wallpapers**: Place images in `~/.config/wallpapers/`
- **Themes**: Use `pywal` or edit `~/.cache/wal/colors-*` files
- **Keybindings**: Modify `~/.config/hypr/hyprland.conf`
- **Shell config**: Edit `/etc/nixos/dotfiles/fish/config.fish`

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to:
- 🐛 [Report bugs](https://github.com/ass-sudo/nix-dotfiles/issues)
- 💡 [Request features](https://github.com/ass-sudo/nix-dotfiles/issues)
- 🔧 [Submit pull requests](https://github.com/ass-sudo/nix-dotfiles/pulls)

---

## 🙏 Acknowledgments

- [NixOS](https://nixos.org/) - For the amazing declarative package manager
- [Hyprland](https://hyprland.org/) - For the beautiful Wayland compositor
- [r/unixporn](https://reddit.com/r/unixporn) - For inspiration and community

---

<div align="center">

### ⭐ Star this repo if you find it helpful!

**Made with by [ass-sudo](https://github.com/ass-sudo)**

[![GitHub](https://img.shields.io/badge/GitHub-ass--sudo-181717?style=for-the-badge&logo=github)](https://github.com/ass-sudo)

---

## 📝 License

This project is licensed under the **GNU General Public License v3.0**.

See the [LICENSE](LICENSE) file for details.

```
Copyright (C) 2025 ass-sudo

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.
```

</div>
