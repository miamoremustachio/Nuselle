- Update the mirror list:

```bash
reflector --verbose -p http,https --sort -l 30 --fastest 10 --save /etc/pacman.d/mirrorlist
```