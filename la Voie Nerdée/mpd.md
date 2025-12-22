# 🛠️ Setup

MPD use the `mpd.conf` file which can be located in one of two paths depending on the setup:

1. `~/.config/mpd/mpd.conf` in per-user configuration mode
2. `/etc/mpd.conf` in system-wide configuration mode

## 👤 Per-user config

- Copy the config file included in the package to the MPD's config location:

```bash
cp /usr/share/doc/mpd/mpdconf.example.gz ~/.config/mpd/
gzip -d mpdconf.example.gz
mv mpdconf.example mpd.conf
```

You can use it as a starting point to create your own config.

- Create all the directories you've manually pointed to in config file:

```bash
mkdir <playlist_dir>
mkdir <state_dir>
```

- Start the service:

```bash
systemctl --user start mpd.service
# Enable it to auto-start mpd on login
```



[^1]: Sources:
	https://wiki.archlinux.org/title/Music_Player_Daemon
	https://mpd.readthedocs.io/en/stable/user.html#
