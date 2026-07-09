*Backports* in [[apt]] are recompiled packages from [testing](https://wiki.debian.org/DebianTesting) (mostly), so they will run without new libraries on a stable Debian distribution.

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
