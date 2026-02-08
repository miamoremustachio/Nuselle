## 📋 Example partitions scheme

| _**Mount point**_ | _**Partition type**_                                                          | _**Suggested size**_                                                          |
| ----------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `/boot/efi`       | [EFI system partition](https://wiki.archlinux.org/title/EFI_system_partition) | 1 GB                                                                          |
| `[SWAP]`          | Linux swap                                                                    | 4GB is ok if you don’t plan to use hibernation, otherwise stick to 1.5 of RAM |
| `/`               | Linux x86-64 root                                                             | Remainder of the device _(at least 30 GB)_                                    |

## 🔧 Partition formatting

- Root:

```bash
mkfs.ext4 /dev/<root_partition>
```

- EFI:

```bash
mkfs.fat -F 32 /dev/<efi_system_partition>
```

> ⚠️
   _Only format the EFI system partition if you created it during the partitioning step. If there already was an EFI system partition on disk beforehand, reformatting it can destroy the boot loaders of other installed operating systems._
>

Swap doesn’t need to be formatted manually, but initialization is required:

```bash
mkswap /dev/<swap_partition>
```