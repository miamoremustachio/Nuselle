- Root:

```bash
mount /dev/<root_partition> /mnt
```

- EFI:

```bash
mount --mkdir /dev/<efi_system_partition> /mnt/boot/efi
```

Enable a swap volume:

```bash
swapon /dev/<swap_partition>
```