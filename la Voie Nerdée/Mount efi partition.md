- Find your ESP’s UUID:

```bash
lsblk -f
```

- Create the mount point if it doesn’t exist:

```bash
sudo mkdir -p /boot/efi
```

- Edit `/etc/fstab` and add a new line in the bottom:

```bash
# /etc/fstab
UUID=<YOUR_ESP_UUID>  /boot/efi  vfat  umask=0077  0  2
```

- Test

```bash
sudo mount -a
```