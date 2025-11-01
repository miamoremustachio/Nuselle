*Swap space* is a a substitute for physical memory that allows the [[Operating systems|OS]] to temporarily move inactive memory pages from RAM to a designated area on the hard drive.
It ensures the OS to run even when RAM is full, preventing system crashes & slowdowns.

The data interchange process is called *swapping*, the rate and assertiveness of which are determined by a parameter called *[[swappiness]]*.

## Increase/Decrease Swap Space

> ⚠️ It is highly recommend to work with partitions only inside the live USB to prevent data lose and corruption

- Check existing swap space:
```bash
swapon -s
```

- disable swap volume:
```bash
sudo swapoff /dev/<swap_path>
```

- Use a partitioning utility such as [[cfdisk]] to shrink/expand the swap partition
- Update the partition table:
```bash
sudo mkswap /dev/<swap_path>
```

- Enable the swap space:
```bash
sudo swapon /dev/<swap_path>
```




[^1]: Sources:
	https://phoenixnap.com/kb/swap-memory
