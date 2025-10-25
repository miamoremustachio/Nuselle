
### 1️⃣ Single-boot

- Install GRUB:

```bash
grub-install --target=x86_64-efi --bootloader-id=grub_uefi --recheck
```

### ☯️ Dual-boot

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