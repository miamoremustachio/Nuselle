---
cssclasses:
  - banner
  - banner-fade
---
![[arch-linux-debian-ubuntu-os-tan-hd-wallpaper-a08cf34c2bf7ce38232f4be61e4bc266.jpg|banner]]
> [!banner-icon] 🩵
> 
# 🛠️ Installation

1. [Download](https://archlinux.org/download/) an ISO and [[GnuPG|verify]] the checksum
2. Check ISO filehash:

```bash
sha512sum --check --ignore-missing <sum_file> # same for sha256sum, md5sum etc.
```

3. [[💿 dd|Create]] the installation medium
4. Disable secure boot
5. Set the keyboard font:

```bash
setfont <font_name> # ter-132n is great if you don't know which to choose
```

6. [[iwctl|Connect]] to the network
7. Synchronize package databases:

```bash
pacman -Sy
```

8. Use [[timedatectl]] to ensure the system clock is synchronized
9. Create [[Partitioning|partitions]]
	*(Use [[cfdisk]] to modify partition tables)*
10. [[Partitioning#🔧 Partition formatting|Format]] and [[Mounting|mount]] partitions:

- Root:

```bash
mount /dev/<root_partition> /mnt
```

- EFI:

```bash
mount --mkdir /dev/<efi_system_partition> /mnt/boot/efi
```

11. Enable a swap volume:

```bash
swapon /dev/<swap_partition>
```

12. Select the [[reflector|mirrors]]
13. Use [[pacman#pacstrap|pacstrap]] to install the OS
14. Generate an fstab file:

```bash
genfstab -U /mnt >> /mnt/etc/fstab
# Check the resulting `/mnt/etc/fstab` file and edit it in case of errors.
```

15. Change root into the new system:

```bash
arch-chroot /mnt
```

16. Set the time zone:

```bash
ln -sf /usr/share/zoneinfo/<region>/<city> /etc/localtime

# Run hwclock to generate /etc/adjtime:
hwclock --systohc
```

17. Set up systemd-timesyncd to prevent clock drift and ensure accurate time
18. Generate [[🌎 Locales|locales]]:
- Edit `/etc/locale.gen` and uncomment all the needed UTF-8 locales
- Generate locales:

```bash
locale-gen
```

- Create the `/etc/locale.conf` file and set the LANG variable accordingly:

```bash
LANG=en_US.UTF-8 # for example
```

19. Enable [[Network management|network manager]]
20. Set root password:

```bash
passwd
```

> 💡
It’s also a good idea to lock the root password after setting it by running `passwd -l root`

21. Install bootloader (e.g. [[grub]] or [[rEFInd]])
22. Exit the chroot environment by typing `exit` or pressing Ctrl+d
23. Finally, restart the machine by typing `reboot`

# 🫧 Post-install steps

- Add [[Users#User adding|users]]
- [[Network management#🌐 Connect to the internet|Connect]] to the internet



[^1]: Sources:
	[https://wiki.archlinux.org/title/Installation_guide#](https://wiki.archlinux.org/title/Installation_guide#)
	https://wiki.archlinux.org/title/General_recommendations
	[https://www.youtube.com/watch?v=c2Y2OHkbE4Y&t=1185s](https://www.youtube.com/watch?v=c2Y2OHkbE4Y&t=1185s)
	[https://www.youtube.com/watch?v=O28sURKsUdA](https://www.youtube.com/watch?v=O28sURKsUdA)
