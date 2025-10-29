Uncomment the relevant line in `/etc/systemd/timesyncd.conf`

```bash
# To verify your configuration:
timedatectl show-timesync --all

# To enable and start it:
timedatectl set-ntp true
```