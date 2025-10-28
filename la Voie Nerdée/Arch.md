---
cssclasses:
  - banner
  - banner-fade
---
![[arch-linux-debian-ubuntu-os-tan-hd-wallpaper-a08cf34c2bf7ce38232f4be61e4bc266.jpg|banner]]
> [!banner-icon] 🩵

# 🛠️ Installation

1. [Download](https://archlinux.org/download/) an ISO
2. Download the signing key from WKD:

```bash
gpg --auto-key-locate clear,wkd -v --locate-exter nal-key pierre@archlinux.org
```

3. Create the [[💿 Installation media]]
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
10. Use [[pacstrap]] to install the OS
11. Generate an [[fstab]] file
12. Change root into the new system:

```bash
arch-chroot /mnt
```

13. Set the time zone:

```bash
ln -sf /usr/share/zoneinfo/<region>/<city> /etc/localtime

# Run hwclock to generate /etc/adjtime:
hwclock --systohc
```

14. Set up systemd-timesyncd to prevent clock drift and ensure accurate time:

```bash
# uncomment the relevant line in /etc/systemd/timesyncd.conf

# To verify your configuration:
timedatectl show-timesync --all

# To enable and start it:
timedatectl set-ntp true
```

15. Generate [[🌎 Locales|locales]]
16. Enable [[NetworkManager]]
17. Set root password:

```bash
passwd
```

> 💡
It’s also a good idea to lock the root password after setting it by running `passwd -l root`


18. Add [[👥 Users|users]]
19. Exit the chroot environment by typing `exit` or pressing Ctrl+d
20. Finally, restart the machine by typing `reboot`

# 🫧 Post-install steps

- Install [[grub]]
- [[NetworkManager#🌐 Connect to the internet|Connect]] to the internet


[^1]: Sources:
	[https://wiki.archlinux.org/title/Installation_guide#](https://wiki.archlinux.org/title/Installation_guide#)
	[https://www.youtube.com/watch?v=c2Y2OHkbE4Y&t=1185s](https://www.youtube.com/watch?v=c2Y2OHkbE4Y&t=1185s)
	[https://www.youtube.com/watch?v=O28sURKsUdA](https://www.youtube.com/watch?v=O28sURKsUdA)
