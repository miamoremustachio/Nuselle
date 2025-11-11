## 🖼️ Rebuild icon cache

- Command Prompt (🛡️Run as administrator):

```powershell
cd %homepath%\AppData\Local\Microsoft\Windows\Explorer

# Kill the Explorer
taskkill /f /im explorer.exe

# Delete cache
del iconcache* 

# Check
dir iconcache*

# Revive Explorer
explorer.exe
```
