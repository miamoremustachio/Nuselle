# 🪛 Setup

## Remember last boot choice

- Edit `/etc/default/grub`:

```bash
GRUB_DEFAULT=saved
GRUB_SAVEDEFAULT=true
```

- Rebuild GRUB config file:

```bash
sudo update-grub # Debian
sudo grub2-mkconfig -o /boot/grub2/grub.cfg # Fedora
```

# 🎨 Customizing

## Install a theme

- Clone theme to the `/boot/grub/themes`
- Add this line to the GRUB config:

```shell
# /etc/default/grub

GRUB_THEME=<path_to_your_theme.txt>
```

- Rebuild GRUB config file:

```bash
sudo update-grub # Debian
sudo grub2-mkconfig -o /boot/grub2/grub.cfg # Fedora
```
