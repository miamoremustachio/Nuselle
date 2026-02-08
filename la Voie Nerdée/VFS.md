All files in Linux are accessed through the *Virtual File System*, or *VFS*.

VFS acts as an abstract layer that implements a unified interface between the kernel and a specific file system.

It provides user applications with access to various file systems using standard [[system calls]] like `open()`, `read()`, and `write()` for any file in a mounted space regardless of the underlying storage type.