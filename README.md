# dotfiles

Dotfiles para Arch Linux con DriftWM (Wayland).

## Requisitos

### AUR Helper

```bash
sudo pacman -S --needed git base-devel go
cd /tmp && git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si
```

### Paquetes oficiales (pacman)

```bash
sudo pacman -S \
  zsh starship neovim vim \
  waybar rofi swaync swayidle swaylock \
  ghostty kitty \
  cava fastfetch btop htop \
  pipewire pipewire-alsa pipewire-jack pipewire-pulse wireplumber pavucontrol \
  grim slurp wl-clipboard cliphist hyprpicker imv mpv \
  fuzzel wlsunset \
  thunar mousepad nano \
  networkmanager network-manager-applet \
  bluez bluez-utils brightnessctl \
  nwg-look papirus-icon-theme otf-font-awesome ttf-jetbrains-mono ttf-jetbrains-mono-nerd \
  gdm seatd xdg-utils \
  nvidia-open nvidia-utils nvidia-settings
```

### Paquetes AUR (yay)

```bash
yay -S --needed \
  brave-bin \
  driftwm \
  wlogout \
  catppuccin-gtk-theme-mocha \
  catppuccin-cursors-mocha
```

### Oh My Zsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Brave Browser (alternativa)

```bash
curl -fsS https://dl.brave.com/install.sh | sh
```

## Instalacion de los dotfiles

Clona el repo y copia los archivos a tu home:

```bash
git clone https://github.com/nico4348/dotfiles.git ~/dotfiles-repo

# Shell
cp ~/dotfiles-repo/.bashrc ~/
cp ~/dotfiles-repo/.bash_profile ~/
cp ~/dotfiles-repo/.bash_logout ~/
cp ~/dotfiles-repo/.zshrc ~/

# GTK
cp ~/dotfiles-repo/.gtkrc-2.0 ~/

# Configs
cp -r ~/dotfiles-repo/.config/* ~/.config/
```

O usa stow si prefieres symlinks:

```bash
sudo pacman -S stow
cd ~/dotfiles-repo
stow -t ~ .
```

## Tema

- **GTK:** Catppuccin Mocha
- **Cursores:** Catppuccin Mocha
- **Iconos:** Papirus
- **Fuente:** JetBrains Mono Nerd Font
- **WM:** DriftWM
- **Barra:** Waybar
- **Launcher:** Rofi
- **Notificaciones:** SwayNC
- **Terminal:** Ghostty / Kitty
- **Shell:** Zsh + Oh My Zsh + Starship
