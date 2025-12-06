A *user* is an individual or system entity that can log in and access the system.
Users in Linux are managed through unique accounts with assigned [[UID|User IDs]], [[permissions]], and roles.

There are 3 types of users in Linux:

## Root (superuser)

- A special user account intended for administrative purposes
- Has the highest level of access and privileges
- [[UID]] is always `0`
- To run a command as superuser use [[sudo]]

## System users

- Reserved for running services and [[daemons]]
- Use a specific range of [[UID|UIDs]] (`1`-`499` or `1`-`999`, depending on the distro)

## Normal users

- Have their own home directories
- [[UID]] usually starts from `1000`

A list of all user accounts is stored in `/etc/passwd` file, which also contains some useful information like user ID, group ID, etc.
Despite the file name it doesn't actually store users [[Passwords|passwords]]: on modern Unix systems, they are written in `/etc/shadow`, hashed for security reasons.

# 🧑‍🧒 User adding

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

# ✏️ User editing

- Add a comment for a user:

```bash
sudo usermod -c "comment" <username>
```

- Change the home directory of a user:

```bash
sudo usermod -d /home/manav test_user
```
