
### Disable the Internet time updating

1. Settings
2. Time & Language
3. Date & Time
4. **✘ Set time zone automatically**
5. **✘ Set time automatically**

### Add registry key

1. Regedit
2. Navigate to the following key:

```bash
HKEY_LOCAL_MACHINE\\System\\CurrentControlSet\\Control\\TimeZoneInformation
```

1. Right-click the `TimeZoneInformation` key and select New > DWORD (32-bit) Value
2. Name your new value `RealTimeIsUniversal`
3. set its value data to `1` and click "OK"