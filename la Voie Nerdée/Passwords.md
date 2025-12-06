*Passwords* in Linux are stored and managed using secure cryptographic techniques to ensure the confidentiality and integrity of user credentials.
The process involves several steps, including password [[Hash|hashing]], [[Salting|salting]], and storage in a secure file (`/etc/shadow`).

All user passwords are converted into a unique hash using a one-way function, thus it cannot be reversed to obtain the original password.

Most Linux distros use the SHA-512 algorithm for password hashing, although other algorithms like MD5 or SHA-256 may also be used depending on the system configuration.

## 👤 Change password

```bash
passwd

# to override password restrictions:
sudo passwd <username>
```

- It's a good idea to also change the login [[Keyrings|keyring]] password right after changing the user one

## 🔒 Lock password

```bash
passwd -l <username>

# to check if its locked:
sudo grep <username> /etc/shadow

# If a line beginning with `!` or a `*` symbols after a username it signalize that the account is disabled;
# Any other value would indicate a working password
```





[^1]: Sources:
	https://eitca.org/cybersecurity/eitc-is-lsa-linux-system-administration/basic-linux-sysadmin-tasks/user-account-management/examination-review-user-account-management/how-are-passwords-stored-and-managed-in-linux/
