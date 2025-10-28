- Root:

```bash
mkfs.ext4 /dev/<root_partition>
```

- EFI:

> ⚠️
   _Only format the EFI system partition if you created it during the partitioning step. If there already was an EFI system partition on disk beforehand, reformatting it can destroy the boot loaders of other installed operating systems._
>

```bash
mkfs.fat -F 32 /dev/<efi_system_partition>
```

Swap doesn’t need to be formatted manually, but initialization is required:

```bash
mkswap /dev/<swap_partition>
```