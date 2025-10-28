- Edit `/etc/locale.gen` and uncomment all the needed UTF-8 locales
- Generate locales:

```bash
locale-gen
```

- Create the `/etc/locale.conf` file and set the LANG variable accordingly:

```bash
LANG=en_US.UTF-8 # for example
```