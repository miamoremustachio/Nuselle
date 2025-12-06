In Linux, both *hard links* and *soft links* (also known as [[symlinks]]) provide ways to create references to files, but they differ fundamentally in their implementation and behavior:

## 🪨 Hard links

- Point directly to to a specific [[inode]]
- Use same inode number as target
- Cannot be used across file systems
- Cannot link to directories
- Comparatively faster

## 🪶 Soft links

- Point to another file name
- Use inode number that different from target
- Can span file systems
- Can link to directories
- Comparatively slower

![[hard-link-and-soft-link-in-linux_thumbnail.webp]]

