# Gnome

- Install Gnome Themes

```bash
sudo dnf in gnome-themes-extra
```

- Gnome Tweaks >> Appearance >> Legacy applications

# Hyprland
## 🧙‍♂️ GTK (GNOME apps):

```bash
gsettings set org.gnome.desktop.interface color-scheme 'prefer-dark'

sudo pacman -S adw-gtk3
gsettings set org.gnome.desktop.interface gtk-theme 'adw-gtk3-dark'

gsettings get org.gnome.desktop.interface color-scheme # To check
```

- Install xsettingsd (lightweight GNOME settings faker):

```bash
sudo pacman -S xsettingsd
```

- Create `~/.config/xsettingsd/xsettingsd.conf`:

```bash
Net/ThemeName "adw-gtk3-dark"
Gtk/ColorScheme "prefer-dark"
```

- AutoStart it in Hyprland:

```bash
# ~/.config/hypr/hyprland.conf
exec-once = xsettingsd &
```

## Qt apps:

```bash
sudo pacman -S qt5ct qt6ct kvantum kvantum breeze-icons

# ~/.config/environment.d/envvars.conf
QT_QPA_PLATFORMTHEME=qt6ct
QT_STYLE_OVERRIDE=kvantum
```

- Run `kvantummanager` (qt6ct) and pick a dark theme