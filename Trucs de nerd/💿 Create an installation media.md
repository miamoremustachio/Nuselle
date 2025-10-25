 
- Download an ISO: [https://archlinux.org/download/](https://archlinux.org/download/)
- Verify the PGP signature and compare the checksum:

```bash
# Download the signing key from WKD:
gpg --auto-key-locate clear,wkd -v --locate-exter nal-key pierre@archlinux.org
# Verify the signature:
gpg --verify archlinux-2025.09.01-x86_64.iso.sig archlinux-2025.09.01-x86_64.iso
```

- Burn image to a USB drive:

```bash
# Check the mounted USB drive name
lsblk

# Unmount all partitions of the USB drive
umount /dev/sdX*

# Run dd
dd bs=4M if=<path/to/archlinux-version-x86_64.iso> of=/dev/sda conv=fsync oflag=direct status=progress
```