## 🛠️ Config

 `~/.bash_profile`
- Executed only for login interactive shells
- Useful for [[Environment variables]], aliases and functions

`~/.bashrc`
- Executed for non-login interactive shells

Reload the shell after making changes in config files:

```bash
source ~/.bashrc # for example
```

## 🔑 Hotkeys

| *Command*             | *Meaning*                                       |
| --------------------- | ----------------------------------------------- |
| `←`/`→`               | Move one character back/forward                 |
| `Ctrl + →`/`Ctrl + ←` | Move one word back/forward                      |
| `Ctrl + A`/`Home`     | Go to the beginning of command line             |
| `Ctrl + E`/`End`      | Go to the end of command line                   |
| `Tab`                 | Autocomplete                                    |
| `Ctrl + H`            | Delete the character before cursor              |
| `Ctrl + D`            | Delete the character under the cursor           |
| `Ctrl + U`            | Clear all characters before cursor              |
| `Ctrl + K`            | Clear all characters after cursor               |
| `Ctrl + W`            | Delete the word before the cursor               |
| `Alt + D`             | Delete the word after the cursor                |
| `Ctrl + Y`            | Paste previously deleted characters             |
| `Ctrl + T`            | Swap two characters before cursor               |
| `Alt + T`             | Swap current word with previous                 |
| `Alt + U`             | Uppercase characters from cursor to end of word |
| `Alt + L`             | Lowercase characters from cursor to end of word |
| `Alt + ?`             | Display the content of current directory        |
| `Ctrl + C`            | Terminate the current process                   |
| `Ctrl + Z`            | Suspend the current process                     |
| `Ctrl + S`            | Pause the current process                       |
| `Ctrl + Q`            | Resume the current process                      |
| `Ctrl + D`            | Exit shell                                      |

![[moving_cli(1) 1.png]]

# ✒️ Scripting

[[Exit codes]]
[[shebang]]



[^1]: Sources:
	https://www.uwyo.edu/data-science/resources/knowledge-base/what-is-a-bash-profile.html
