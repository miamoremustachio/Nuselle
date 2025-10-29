---
cssclasses:
  - banner
  - banner-fade
---
![[letter_by_ajvl_d847iw5 1.jpg|banner]]
> [!banner-icon] 🐾
# 🛠️ Setting up

## ⌨️ Change layout switching shortcut

1. _Gnome Tweaks_
2. _Keyboard_
3. _Additional Layout Options_
4. _Switching to another layout_ 
	✅ Alt+Shift

**OR**

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

## 🚫 Disable annoying Emoji shortcuts
- Run `$ ibus-setup`
- Go to Emoji tab
- Clear Emoji annotation shortcuts

## Other

- [[🧩 Extensions]]
- [[🌚 Dark theme]]