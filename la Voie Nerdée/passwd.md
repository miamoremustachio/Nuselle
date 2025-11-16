## 👤 Change user password

```bash
passwd

# to override password restrictions:
sudo passwd <username>
```

- It's a good idea to also change the login [[Keyrings|keyring]] password right after changing the user one

## 🔒 Lock root password

```bash
passwd -l root

# to check if its locked:
sudo grep root /etc/shadow

# If a line beginning with `!` or a `*` symbols after `root:` it signalize that the account is disabled
# Any other value would indicate a working password
```