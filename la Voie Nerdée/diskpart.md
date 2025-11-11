## 📌 Standard Windows partition scheme

| _**Partition**_              | _**Type**_ | _**Label**_ | _**Letter**_ | _**Size**_      |
| ---------------------------- | ---------- | ----------- | ------------ | --------------- |
| EFI System Partition         | efi        | `EFI`       | `S`          | at least 100 MB |
| Microsoft Reserved Partition | msr        | -           | -            | 16 MB           |
| Windows Partition            | primary    | `Windows`   | `C`          | at least 64 GB  |

# 🛠️ Usage

## Select object

```powershell
diskpart
list disk
select disk X # Replace X with your SSD number
```
*Object might be either disk, partition or volume* 

## Convert to NTFS

```powershell
clean
convert gpt
```

## Create partitions

```powershell
~~~ EFI System Partition ~~~
create partition efi size=100
format quick fs=fat32 label="EFI"
assign letter=S

~~~ Microsoft Reserved Partition ~~~
create partition msr size=16

~~~ Windows Partition ~~~
create partition primary size=65536
format quick fs=ntfs label="Windows"
assign letter=C
```

> ⚠️ Some commands automatically change the focus: when you create a new partition, the focus immediately switches to it


[^1]: Sources:
	https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/diskpart
