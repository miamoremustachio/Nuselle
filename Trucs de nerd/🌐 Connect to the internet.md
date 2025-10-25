
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