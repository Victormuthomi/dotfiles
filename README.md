# Dotfiles Backup

This repository contains my personal configuration files for a **premium Linux developer environment**, including:

- **Alacritty** – terminal emulator
- **Starship** – terminal prompt
- **Tmux** – terminal multiplexer
- **Neovim** – code editor
- **Zsh** – shell

Backing up these files ensures that your **entire environment can be restored on any machine** quickly and consistently.

## Contents

| File / Folder    | Description                                                           |
| ---------------- | --------------------------------------------------------------------- |
| `alacritty.toml` | Configuration for Alacritty terminal (fonts, colors, fullscreen)      |
| `starship.toml`  | Starship prompt configuration (hostname, directory, git status, time) |
| `.tmux.conf`     | Tmux configuration for splits, keybindings, and status bar            |
| `nvim/`          | Neovim configuration folder, including `init.vim` or `init.lua`       |
| `.zshrc`         | Zsh shell configuration with aliases and environment settings         |

## Restore Instructions

To restore your full development environment on a new machine, simply run this **one command**:

```bash
git clone https://github.com/Victormuthomi/dotfiles.git ~/dotfiles && \
cd ~/dotfiles && \
mkdir -p ~/.config/alacritty && cp alacritty.toml ~/.config/alacritty/ && \
mkdir -p ~/.config && cp starship.toml ~/.config/ && \
cp .tmux.conf ~/ && \
mkdir -p ~/.config && cp -r nvim ~/.config/ && \
cp .zshrc ~/ && \
source ~/.zshrc && \
tmux source ~/.tmux.conf


```

## Keeping Your Dotfiles Updated

Whenever you make changes to your configuration files (Alacritty, Starship, Tmux, Neovim, Zsh), you can **sync them to GitHub** so your backup stays current.

```bash
cd ~/dotfiles
git add .
git commit -m "Update configs"
git push

```
