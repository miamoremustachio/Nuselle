
### 🪞 Select the mirrors

- Update the mirror list

```bash
reflector --verbose -p http,https --sort -l 30 --fastest 10 --save /etc/pacman.d/mirrorlist
```

- Install the base package, Linux kernel and firmware for common hardware:

```bash

# Basic installation:
pacstrap -K /mnt base linux linux-firmware

# Advanced installation:
pacstrap -K /mnt base linux linux-lts linux-headers linux-lts-headers linux-firmware sof-firmware base-devel nano sudo networkmanager bluez bluez-utils curl wget efibootmgr man-db man-pages texinfo
```