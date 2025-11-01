---
cssclasses:
  - banner
  - banner-fade
---
![[arch-linux-debian-ubuntu-os-tan-hd-wallpaper-a08cf34c2bf7ce38232f4be61e4bc266.jpg|banner]]
> [!banner-icon] 🩵

# 🛠️ Installation

1. [Download](https://archlinux.org/download/) an ISO and verify the checksum
2. [[💿 dd|Create]] the installation medium
3. Disable secure boot
4. [[⌨️ Keyboard#Set font|Set]] the keyboard font
5. [[iwctl|Connect]] to the network
6. Synchronize package databases:

```bash
pacman -Sy
```

7. Use [[timedatectl]] to ensure the system clock is synchronized
8. Create [[Partitioning|partitions]]
	*(Use [[cfdisk]] to modify partition tables)*
9. [[Partition formatting|Format]] and [[Mounting|mount]] partitions
10. Select the [[reflector|mirrors]]
11. Use [[pacstrap]] to install the OS
12. Generate an [[fstab]] file
13. Change root into the new system:

```bash
arch-chroot /mnt
```

14. Set the time zone:

```bash
ln -sf /usr/share/zoneinfo/<region>/<city> /etc/localtime

# Run hwclock to generate /etc/adjtime:
hwclock --systohc
```

15. Set up [[systemd-timesyncd]] to prevent clock drift and ensure accurate time
16. Generate [[🌎 Locales|locales]]
17. Enable [[Network management|network manager]]
18. Set [[Superuser|root]] password:

```bash
passwd
```

> 💡
It’s also a good idea to lock the root password after setting it by running `passwd -l root`

19. Install bootloader (e.g. [[grub]] or [[rEFInd]])
20. Exit the chroot environment by typing `exit` or pressing Ctrl+d
21. Finally, restart the machine by typing `reboot`

# 🫧 Post-install steps

- Add [[User adding|users]]
- [[Network management#🌐 Connect to the internet|Connect]] to the internet



[^1]: Sources:
	[https://wiki.archlinux.org/title/Installation_guide#](https://wiki.archlinux.org/title/Installation_guide#)
	https://wiki.archlinux.org/title/General_recommendations
	[https://www.youtube.com/watch?v=c2Y2OHkbE4Y&t=1185s](https://www.youtube.com/watch?v=c2Y2OHkbE4Y&t=1185s)
	[https://www.youtube.com/watch?v=O28sURKsUdA](https://www.youtube.com/watch?v=O28sURKsUdA)
