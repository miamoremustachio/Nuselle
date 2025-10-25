- Create a script file in `/usr/local/bin`

```bash
sudo nano /usr/local/bin/<package>-update.sh
```

```bash
#!/bin/bash

dnf upgrade <package_name> -y
```

- Change file permissions

```bash
sudo chmod 755 /usr/bin/<package>-update.sh
# limits write permissions to owner only (root)
```

- Create a systemd service file

```bash
sudo nano /etc/systemd/system/<package>-update.service
```

```bash
[Unit]
Description=<package> Auto Update Service
After=network-online.target
Wants=network-online.target

[Service]
Type=oneshot
ExecStart=/bin/bash /usr/local/bin/<package>-update.sh

[Install]
WantedBy=multi-user.target
```

Check if service works properly

```bash
systemctl status <package>-update.service

sudo systemctl start <package>-update.service

systemctl status <package>-update.service # again
```

- Enable service

```bash
sudo systemctl enable <package>-update.service
```
