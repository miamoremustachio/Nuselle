- Get your WNIC name:

```bash
station list
```

- _If it says “no devices in station mode”_:

```bash
adapter phy0 set-property Powered on
device wlan0 set-property Powered on
```

- Get the list of networks:

```bash
station <device_name> get-networks
```

- Connect to the network:

```bash
station <device_name> connect <network_name>
# it will ask you for the password if the network is secured
```

- Check the connection with [ping](https://wiki.archlinux.org/title/Ping):

```bash
ping -c 5 example.com
```
