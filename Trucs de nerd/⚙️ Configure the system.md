
- Generate an fstab file:

```bash
genfstab -U /mnt >> /mnt/etc/fstab
```

Check the resulting `/mnt/etc/fstab` file and edit it in case of errors.

- Change root into the new system:

```bash
arch-chroot /mnt
```

- Set the time zone:

```bash
ln -sf /usr/share/zoneinfo/<region>/<city> /etc/localtime

# Run hwclock to generate /etc/adjtime:
hwclock --systohc
```

- Set up systemd-timesyncd to prevent clock drift and ensure accurate time:

```bash
# uncomment the relevant line in /etc/systemd/timesyncd.conf

# To verify your configuration:
timedatectl show-timesync --all

# To enable and start it:
timedatectl set-ntp true
```