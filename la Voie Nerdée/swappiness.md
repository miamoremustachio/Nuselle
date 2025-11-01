Lower swappiness values prioritize keeping data in RAM, while higher swappiness values result in assertive swapping

| Swappiness Value | Swappiness Effect                    |
| ---------------- | ------------------------------------ |
| 0                | Avoid swappiness as much as possible |
| 10-50            | Slightly aggressive swappiness       |
| 50-100           | Moderately aggressive swappiness     |
| > 100            | Very aggressive swappiness           |
## Change swappiness value

- Check the `/proc/sys/vm/swappiness`
- Edit `/etc/sysctl.conf`:
```bash
vm.swappiness = [value]
```

- Apply changes:
```bash
sudo sysctl -p
```



[^1]: Sources:
	https://phoenixnap.com/kb/swappiness
