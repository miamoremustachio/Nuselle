# 🛠️ Installation

## 1️⃣ Single-boot

- Install GRUB:

```bash
grub-install --target=x86_64-efi --bootloader-id=grub_uefi --recheck
```

- Create config file:

```bash
grub-mkconfig -o /boot/grub/grub.cfg
```

## ☯️ Dual-boot

- Install os-prober:

```bash
pacman -S os-prober
```

- Uncomment this line in `/etc/default/grub`:

```bash
GRUB_DISABLE_OS_PROBER=false
```

- Install GRUB:

```bash

grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=Arch
```

- Create config file:

```bash
grub-mkconfig -o /boot/grub/grub.cfg
```

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
