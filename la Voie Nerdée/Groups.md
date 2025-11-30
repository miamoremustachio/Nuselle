In Linux, *groups* are a fundamental mechanism for managing user permissions and access to system resources.
They allow administrators to organize users and assign specific privileges to them, simplifying security management.

The `/etc/group` file contains a list of groups on the system.

# Usage

- Add user to the group:

```bash
sudo usermod -aG <group> <username>
```

- Display groups the user belongs to:

```bash
groups <username>
```