A *symbolic link*, often refers as *symlink*, 

Symlinks always have their permission set to 777 (`rwxrwxrwx`).
It is just a placeholder, because link files do not have their own permissions: they use the same permission set as the target.

# ⛓️ Usage

- Create a symlink:

```bash
ln -s <source_file> <link_name>
```