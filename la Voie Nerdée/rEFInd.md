# 🛠️ Install

```bash
sudo dnf install refind
sudo refind-install
```

# 🗑️ Uninstall

```bash
sudo refind-install --uninstall
```

Then:
- Use `sudo grub2-install --target=x86_64-efi --efi-directory=/boot/efi` to reinstall GRUB as the default

- Or pick GRUB from your firmware’s boot menu.