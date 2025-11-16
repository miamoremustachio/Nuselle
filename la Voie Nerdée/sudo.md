Allows an authorized user to run a program as another user
*([[Superuser|superuser]] by default)*
It temporarily elevates a user's [[Privileges|privileges]] to run a specific command.

## 🗝️ Usage

- [[User adding|Add]] user to sudoers:

```bash
sudo usermod -aG sudo <username>
getent group sudo # check if user was added
```

- Show user's groups:

```
groups <username>
```

- Edit a file with root [[Privileges|privileges]]:

```bash
sudoedit # same as sudo -e
```

This will create a temporary copy of that file which is owned by *your* user account, not the root user, and, if being modified, save the file to its original location.
It allows to preserve user configurations, themes and plugins while editing the file.