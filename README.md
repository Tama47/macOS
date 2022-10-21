# macOS

### Remove iCloud Downloads
```bash
cd ~/Library/Mobile\ Documents/com~apple~CloudDocs/
find . -type f -exec brctl evict {} \;
```

### Hide/Unhide Files
```bash
chflags hidden 
```
```bash
chflags nohidden
```
