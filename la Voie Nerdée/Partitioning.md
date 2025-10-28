**List of required partitions:**

1. root directory `/`
2. EFI system partition `/boot/efi` _(if hasn’t exist already)_
3. Swap partition
4. Home partition _(optional)_

### 📋 Partitions layout example

| _**Mount point**_ | _**Partition type**_                                                          | _**Suggested size**_                                                          |
| ----------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `/boot/efi`       | [EFI system partition](https://wiki.archlinux.org/title/EFI_system_partition) | 1 GB                                                                          |
| `[SWAP]`          | Linux swap                                                                    | 4GB is ok if you don’t plan to use hibernation, otherwise stick to 1.5 of RAM |
| `/`               | Linux x86-64 root                                                             | Remainder of the device _(at least 30 GB)_                                    |
