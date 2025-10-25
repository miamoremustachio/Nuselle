
- Create new user:

```bash
useradd -mg users -G wheel,audio,video,storage -s /bin/bash <username>
```

- Set user password:

```bash
passwd <username>
```

- Edit visudo:

```bash
EDITOR=nano visudo
```

- Uncomment the following line:

```bash
%wheel ALL=(ALL:ALL) ALL
```