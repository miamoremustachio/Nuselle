- Burn image to a USB drive:

```bash
# Check the mounted USB drive name
lsblk

# Unmount all partitions of the USB drive
umount /dev/sdX*

# Run dd
dd bs=4M if=<path_to_the_image.iso> of=/dev/sda conv=fsync oflag=direct status=progress
```