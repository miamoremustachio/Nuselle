# 🪺 Sources

The main APT sources configuration file is `/etc/apt/sources.list.d/debian.sources`

If you add a new source, it's best to add a new file: put it in the same directory, preferably with a name that describes the source and ends with .sources (e.g. `/etc/apt/sources.list.d/neurodebian.sources` for [NeuroDebian](https://neuro.debian.net/))

## Formats

 `debian.sources`
- Modern and stylish~
- Recommended to use since [Trixie](https://wiki.debian.org/DebianTrixie)

`sources.list`
- Older and less readable
- Likely to be deprecated in a future release

## Examples

For a working configuration with all suites and components enabled, see:

- `/usr/share/doc/apt/examples/debian.sources` ([trixie](https://wiki.debian.org/DebianTrixie) and later)
- `/usr/share/doc/apt/examples/sources.list` ([bookworm](https://wiki.debian.org/DebianBookworm) and earlier)

## Upgrading to the new format

```bash
sudo apt modernize-sources
```

Then compare your new files to the .list.bak files your old configs has been renamed to.

# 🔧 Troubleshooting

## Fetch failures

If apt refuses to install/update a package due to 404 error, refreshing package information cache may helps:

```bash
sudo rm -r /var/lib/apt/lists
```

Then `sudo apt update` will recreate the lists directory on the next run.

# ♻️ Autoremove

While `apt autoremove` is generally safe because it only targets orphan dependencies that no other package explicitly requires, a broken dependency chain or a deleted desktop metapackage can trick `apt` into deleting your entire user interface or critical system applications

1. Perform a Dry Run (Simulation)

Before executing any actual deletions, simulate the command. This prints exactly what `apt` plans to remove without making changes to your system.

```bash
apt -s autoremove
```

2. Scan the Output for Core Applications

When you review the simulated list or run `sudo apt autoremove`, look closely at what is targeted.

>[!success] Safe to remove
>- Libraries (`lib...`)
>- Old Linux kernels (`linux-image-...`)
>- Headers

>[!caution] Danger zone
>- Metapackages (`ubuntu-desktop`, `gnome-shell`, `gdm3`)

if `apt` wants to remove an application you still need, it means the package was automatically installed as a dependency in the past, and its parent package was removed.
You can save it by explicitly marking it as manually installed:

```bash
sudo apt-mark manual <package_name>
```

>[!Tip]
> Running `install` on an already installed package simply flips its status from "automatic" to "manual" without downloading it again

Once marked manual, `apt autoremove` will ignore it

4. Check for Metapackages
A common way systems break is when a user uninstalls a minor component of a desktop environment (e.g., a default text editor or email client). This uninstalls the massive "metapackage" that bundles the desktop environment together. The next time you run `autoremove`, `apt` thinks the entire desktop environment is no longer needed.


5. Know How to Recover

If you accidentally ran the command and your system behaves strangely or boots into a black terminal screen, do not panic

Open your package manager history log to see exactly what was removed:

```
cat /var/log/apt/history.log
```

Reinstall the missing desktop environment or packages directly from the command line



[^1]: Sources:
	https://wiki.debian.org/SourcesList
	https://fastfox.pro/blog/tutorials/apt-autoremove-safe-cleanup/