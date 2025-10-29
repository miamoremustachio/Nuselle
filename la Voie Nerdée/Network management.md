- Create the hostname file:

```bash
nano /etc/hostname #write your hostname in it
```

- Edit `/etc/hosts`:

```bash
127.0.0.1    localhost
::1          localhost
127.0.1.1    <hostname>.localdomain    <hostname>
```

- Enable network manager:

```bash
systemctl enable NetworkManager
```

## 🌐 Connect to the internet

```bash
nmcli device wifi list # list available networks 
sudo nmcli device wifi connect <network_SSID> password <network_password>
```

### Troubleshooting

- Delete the network connection:

```bash
nmcli connection delete <network_SSID>
# Then reconnect again
```

- Config regulatory database:

```bash
sudo pacman -S wireless-regdb

sudo nano /etc/conf.d/wireless-regdom # Uncomment the appropriate region

reboot

# Confirm if it really applied:
iw reg get
```

- Decrease the number of parallel downloads:

```bash
sudo nano /etc/pacman.conf
```