# 🪺 Sources

The main APT sources configuration file is `/etc/apt/sources.list.d/debian.sources`

If you add a new source, it's best to add a new file: put it in the same directory, preferably with a name that describes the source and ends with .sources (e.g. `/etc/apt/sources.list.d/neurodebian.sources` for [NeuroDebian](https://neuro.debian.net/))

## 💽 Formats

 `debian.sources`
- Modern and stylish~
- Recommended to use since [Trixie](https://wiki.debian.org/DebianTrixie)

`sources.list`
- Older and less readable
- Likely to be deprecated in a future release

## 🦜 Examples

For a working configuration with all suites and components enabled, see:

- `/usr/share/doc/apt/examples/debian.sources` ([trixie](https://wiki.debian.org/DebianTrixie) and later)
- `/usr/share/doc/apt/examples/sources.list` ([bookworm](https://wiki.debian.org/DebianBookworm) and earlier)

## 🗽 Upgrading to the new format

```bash
sudo apt modernize-sources
```

Then compare your new files to the .list.bak files your old configs has been renamed to.

# ⚓ Backports

*Backports* are recompiled packages from [testing](https://wiki.debian.org/DebianTesting) (mostly), so they will run without new libraries on a stable Debian distribution.

##  🛠️ Setup

- Create `/etc/apt/sources.list.d/debian-backports.sources`:

```bash
Types: deb deb-src
URIs: http://deb.debian.org/debian
Suites: trixie-backports
Components: main contrib non-free non-free-firmware
Enabled: yes
Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg
```
  
- Run `apt update`

## 🚢 Usage

All backports are deactivated by default.

To find out if a backport of a certain Debian package exists you can use Debian's web-based [package search](https://packages.debian.org) or search its name with the `apt search` command.

You can also view all available versions of a package by running `apt show package-name -a`.

- To install something from backports run:

```bash
apt install <package>/trixie-backports
```

- If you also want missing dependencies to be installed from trixie-backports:

```bash
apt install -t trixie-backports <package>
```

- And of course aptitude may also be used:

```bash
aptitude install <package>/trixie-backports
```




[^1]: Sources:
	https://wiki.debian.org/SourcesList
