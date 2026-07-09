## 🛠️ Set up

- Make zsh the default shell:

```bash
chsh -s $(which zsh)
```

>[!info] Note
>This operation requires zsh to be in your authorized shells list (`/etc/shells`)

- Log out/in to restart the default shell
- Test that it worked:

```bash
echo $SHELL # Expected `/bin/zsh` or similar
```




[^1]: Sources:
	https://github.com/ohmyzsh/ohmyzsh/wiki
