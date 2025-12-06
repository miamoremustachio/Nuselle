Linux file permissions is a core of the system’s security model.
They define who can read, write, or execute files and directories, ensuring only authorized users can access sensitive data.

Every file or directory has three types of permissions:

- **Read (r):** View the file or a directory content
- **Write (w):** Modify a file or change files in a directory
- **Execute (x):** Execute a file or enter a directory

Those permissions are assigned to three categories of users:

- **User:** One who created the file
- **Group:** Users belonging to a shared group
- **Others:** Everyone else on the system

Use the `ls` command with `-l` flag to view the permissions set for the files and directories

# 🔏 Change permissions

```bash
chmod <who>=<permissions> <file>

# Where `who` means who is being given the permission: user (u), group (g), others (o), or all the above (a)
```

You can also add or subtract permissions from an existing set using `+` or `-` instead of `=`.
For example:

```bash
chmod u+x foobar

# Add execution rights to the user
```

`chmod` can also set permissions using **octal system**.
It allows you to edit permissions for the owner, group, and others at the same time.

The basic code structure is this:

```bash
chmod xxx <file>
```

Where `xxx` is a 3-digit number where each digit can be anything from 0 to 7. The first digit applies to permissions for owner, the second digit applies to permissions for group, and the third digit applies to permissions for all others.

![[fb1a898a-8440-430e-8ffa-3612d0555e6f_1768x1288.png]]



[^1]: Sources:
	https://wiki.archlinux.org/title/File_permissions_and_attributes
	https://www.geeksforgeeks.org/linux-unix/set-file-permissions-linux/
