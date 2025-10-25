
- Edit `/etc/locale.gen` and uncomment all the needed UTF-8 locales
- Generate the locales by running:

```bash
locale-gen
```

- Create the `/etc/locale.conf` file and set the LANG variable accordingly:

```bash
LANG=en_US.UTF-8 # for example
```