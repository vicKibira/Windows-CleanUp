## Cleaning my windows machine

###  1. Clean user temporary files

```bash
Remove-Item "$env:TEMP\*" -Recurse -Force -ErrorAction SilentlyContinue
```

###  2. Clean Windows temporary files

```bash
Remove-Item "C:\Windows\Temp\*" -Recurse -Force -ErrorAction SilentlyContinue
```

###  3. Clean Windows component store

```bash
DISM.exe /Online /Cleanup-Image /StartComponentCleanup
```

###   4. Launch Windows Disk Cleanupe

```bash
cleanmgr.exe
```
