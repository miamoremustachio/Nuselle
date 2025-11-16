*Keyring* is a security feature that stores passwords, [[SSH keys]], [[GnuPG|GPG keys]], and [[certificates]] in encrypted form.

By default keyrings use the user’s login password to unlock. If the login password has changed or auto-login is enabled, they may not unlock automatically.
To fix this, you can update the keyring's password to match your new one.

# Gnome
## ☘️ Update login keyring

- Open Seahorse *("Passwords and Keys")*
- > Login keyring
- > Change Password

## 🪦 In case you don't remember old password

- Remove existing keyring:

```bash
rm ~/.local/share/keyrings/login.keyring && rm ~/.local/share/keyrings/user.keystore
```

- Reload the Gnome keyring daemon:

```bash
systemctl --user restart gnome-keyring-daemon.service
```