---
cssclasses:
  - banner
  - banner-fade
---
![[letter_by_ajvl_d847iw5 1.jpg|banner]]
> [!banner-icon] 🐾
# 🛠️ Setting up

## ⌨️ Change layout switching shortcut

```bash
$ gsettings set org.gnome.desktop.wm.keybindings switch-input-source "['<Shift>Alt_L']"
$ gsettings set org.gnome.desktop.wm.keybindings switch-input-source-backward "['<Alt>Shift_L']"
```

## ⛅ Reset weather locations

```bash
gsettings reset org.gnome.Weather locations
```

## 📟 Set default terminal

```bash
gsettings set org.gnome.desktop.default-applications.terminal exec desired_terminal
```

## 📂 Set Files shortcut

```bash
# Paste this to the custom shortcut command
nautilus --new-window
```

## 🚫 Disable annoying Emoji shortcuts
- Run `ibus-setup`
- Go to Emoji tab
- Clear Emoji annotation shortcuts

## 🪄 Download & Install incompatible extensions

```bash
gsettings set org.gnome.shell disable-extension-version-validation true
```

## Other

- [[🌚 Dark theme]]