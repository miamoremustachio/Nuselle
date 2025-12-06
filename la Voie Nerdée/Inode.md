An *inode* (short for "index node") is a data structure in a Linux file system that stores metadata about a file or directory, such as size, permissions, owner, and timestamps.
Each inode points to the disk blocks where the file data is stored.

Inodes don't contain file names - they are stored separately in file directories.

Typically about 1% of the total disk space is reserved for the inode table.
The number of inodes In ext4 file system is determined at the stage of a new file system formatting.