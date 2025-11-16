- Create new user:

```bash
su root # switch to superuser
adduser <username>

# for Arch:
useradd -mg users -G wheel,audio,video,storage -s /bin/bash <username>
```

- Set user password:

```bash
passwd <username>
```

- Edit [[visudo]] and uncomment the following line:

```bash
%wheel ALL=(ALL:ALL) ALL
```