# macOS

### Network
```bash
curl ifconfig.me && echo
```
```bash
speedtest --server-id=50679
```

### Remove iCloud Downloads
```bash
cd ~/Library/Mobile\ Documents/com~apple~CloudDocs/
find . -type f -exec brctl evict {} \;
```
```bash
cd ~/Library/Mobile\ Documents/com~apple~CloudDocs/
killall bird && rm -rf CloudDocs
```

### Hide/Unhide Files
```bash
chflags hidden 
```
```bash
chflags nohidden 
```

### Compress without .DS_Store and __MACOSX
```bash
zip -r Archive.zip . -x ".*" -x "__MACOSX"
```

### Reset and Lock Size of Dock
```bash
defaults write com.apple.dock tilesize -integer 64; killall Dock
```
```bash
defaults write com.apple.dock size-immutable -bool yes; killall Dock
```

### Python SimpleHTTPServer
```bash
python -m SimpleHTTPServer
```

### Create a RAM Disk
```bash
diskutil erasevolume HFS+ "RAM Disk" `hdiutil attach -nomount ram://2048000`
```

### Prevent creation of .DS_Store files on network shares
```bash
defaults write com.apple.desktopservices DSDontWriteNetworkStores -bool TRUE
```
