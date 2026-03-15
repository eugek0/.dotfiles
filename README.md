# Dotfiles

Personal configuration files for my Linux environment.

This repository contains configuration files for my development environment, window manager setup, terminal tools, and other applications.
All files are managed using **GNU Stow** to create symbolic links in the home directory.

## Requirements

Before installing, make sure the following tools are installed:

* GNU Stow
* Git
* Zsh
* GDM
* Niri
* DMS
* Kitty
* Yay

Example for Arch Linux:

```bash
sudo pacman -S --needed git base-devel && git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si
sudo pacman -Suy stow zsh niri xwayland-satellite xdg-desktop-portal-gnome xdg-desktop-portal-gtk kitty dms-shell-bin matugen cava qt6-multimedia-ffmpeg
systemctl --user add-wants niri.service dms
```

## Installation

Clone the repository:

```bash
git clone https://github.com/eugek0/.dotfiles.git ~/.dotfiles
cd ~/.dotfiles
```

Then create symlinks using **stow**:

```bash
stow .
```

## Updating

To apply changes after editing configs:

```bash
stow -R .
```

## Removing configs

To remove symlinks:

```bash
stow -D <package>
```

Example:

```bash
stow -D zsh
```

## License

MIT
