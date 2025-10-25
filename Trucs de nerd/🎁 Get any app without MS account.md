
`$ winget install %APPID% -s msstore`,

where `%APPID%` is id from [https://apps.microsoft.com/](https://apps.microsoft.com/)  
(after [detail/]())

**OR**

- Go to [https://store.rg-adguard.net/](https://store.rg-adguard.net/)
- Past the link from the Microsoft Store app in search
- Download desired build:

```bash
irm "<download_link>" -o <output_name>
```

- Open PowerShell as Administrator
- Install the app:

```bash
Add-AppxPackage <executable_location>
```
