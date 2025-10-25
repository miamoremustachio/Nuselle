## 🔧 Install

```bash
sh -c "$(curl -fsSL <https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh>)"
```

## 🧩 Set up plugins

- zsh-autosuggestions

```bash
git clone <https://github.com/zsh-users/zsh-autosuggestions> ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

- zsh-syntax-highlighting

```bash
git clone <https://github.com/zsh-users/zsh-syntax-highlighting.git> ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

- zsh-autocomplete

```bash
git clone --depth 1 -- <https://github.com/marlonrichert/zsh-autocomplete.git> $ZSH_CUSTOM/plugins/zsh-autocomplete
```

At the end, enable all of the installed plugins:

- Open ~/.zshrc
- Find the line which says `plugins=(git)`
- Replace that line with

```bash
plugins=(
	git
	zsh-autosuggestions
	zsh-syntax-highlighting
	zsh-autocomplete
)
```

## 🖍️ Disable path highlighting

```bash
# edit ~/.zshrc

ZSH_HIGHLIGHT_STYLES[path]='none'
```