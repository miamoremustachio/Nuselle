*Mounting* is a process of making a file system accessible to the OS by attaching it to a specific directory (the mount point).

The `/etc/fstab` is a system configuration file that defines how disk partitions, remote file systems and other storage devices should be mounted.

All the devices specified in the `/etc/fstab` are mounted automatically at system boot.

## 🪢Usage

- Mount a filesystem:
```bash
sudo mount <device> <mountpoint> # For a current session

# To mount a fs permanently, edit /etc/fstab
```

- Unmount a filesystem:
```bash
sudo umount [<device>|<mountpoint>]
```