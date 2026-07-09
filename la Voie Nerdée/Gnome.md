---
cssclasses:
  - banner
  - banner-fade
---
![[letter_by_ajvl_d847iw5.jpg|banner]]
> [!banner-icon] 🐾
# 🛠️ Set up

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
gsettings set org.gnome.desktop.default-applications.terminal exec kitty
#for example
```

## 📂 Set Files shortcut

```bash
# Paste this to the custom shortcut command
nautilus --new-window
```

## 🔥 Enable Nautilus file picker in Firefox

- `about:config`
- Set `widget.use-xdg-desktop-portal.file-picker` to `1`

## 🚫 Disable annoying Emoji shortcuts
- Run `ibus-setup`
- Go to Emoji tab
- Clear Emoji annotation shortcuts

## 🪄 Download & Install incompatible extensions

```bash
gsettings set org.gnome.shell disable-extension-version-validation true
```
