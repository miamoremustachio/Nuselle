
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