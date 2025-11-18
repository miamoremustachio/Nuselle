The *Linux Filesystem Hierarchy Standard (FHS)* defines the directory structure in Unix-like operating systems.
It is maintained by the [Linux Foundation](https://www.linuxfoundation.org/).

## `/ (root)`

The top-most directory in a file tree where all other directories branching from
*(not to be confused with `/root`, which is root user’s home directory)*

## `/bin`

Essential commands and binaries that need to be available in [[Single user mode|single-user mode]], 
(e.g. `ls`, `cat`, `grep`)

## `/boot`

Bootloader and kernel files
(e.g. [[initrd]], [[vmlinux]], [[grub]]) 

## `/dev`

Device files
(e.g. USB, disk [[Partitioning|partitions]], `/dev/null`)

## `/etc`

System-wide config files

## `/home`

User's home directories which stores their personal files, downloads, user settings etc.

Each user can create, delete, or modify files only in their own home directory and cannot access others’ home directories

## `/lib`

Libraries required for binaries in `/bin` and `/sbin`

## `/media`

Mount points for removable devices

## `/mnt`

Temporarily [[Mounting|mounted]] filesystems

## `/opt`

Third-party software and packages

### `/proc`

Virtual filesystem providing detailed information about system [[processes]] and [[🌰 Kernel|kernel]]

## `/root`

Root user's home directory

## `/run`

Runtime data: information about the system state since the last boot, including files needed for [[daemons]]

## `/sbin`

Essential *system* binaries used for administrative purposes
(e.g. `iptables`, `reboot`, `fdisk`, `swapon`)

## `/srv`

Data for services provided by the system, such as websites, FTP files, and other network services

## `/sys`

Information about devices, drivers, and some kernel features

## `/tmp`

Temporary files

## `/usr`

_Secondary hierarchy_ for user data; contains the majority of user utilities and applications

#### `/usr/bin`

Non-essential command binaries for all users

## `/var`

Variable files, such as logs, spool files, and temporary e-mail files


![[GQLCKqJbMAA_7U3.jpg]]
