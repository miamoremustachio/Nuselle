
1. *→ Command Prompt (🛡️Run as administrator)*
2. `cd %homepath%\\AppData\\Local\\Microsoft\\Windows\\Explorer`
3. Kill the Explorer:

```
taskkill /f /im explorer.exe
```

4. Delete cache:

```
del iconcache*
```

5. Check:

```
dir iconcache*
```

6. Revive Explorer:
```
explorer.exe
```