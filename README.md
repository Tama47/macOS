# macOS

### Compress without .DS_Store and __MACOSX
```bash
zip -r Archive.zip . -x ".*" -x "__MACOSX"
```

### Create a RAM Disk
```bash
diskutil erasevolume HFS+ "RAM Disk" `hdiutil attach -nomount ram://2048000`
```

### Hide/Unhide Files
```bash
chflags hidden 
```
```bash
chflags nohidden 
```

### Prevent creation of .DS_Store files on network shares
```bash
defaults write com.apple.desktopservices DSDontWriteNetworkStores -bool TRUE
```

### Python Apache Server
Command to restart mac apache server:
```bash
sudo apachectl restart
```
Command to start mac apache server:
```bash
sudo apachectl start
```
Command to stop mac apache server:
```bash
sudo apachectl stop
```
Edit the Apache configuration file:
```bash
sudo nano /etc/apache2/httpd.conf
```

### Python SimpleHTTPServer
```bash
python -m SimpleHTTPServer
```

### Remove iCloud Downloads
```bash
cd ~/Library/Mobile\ Documents/com~apple~CloudDocs/
killall bird && rm -rf CloudDocs
find . -type f -exec brctl evict {} \;
```

### Reset Bluetooth Module
```bash
sudo pkill bluetoothd
```

### Reset and Lock Size of Dock
```bash
defaults write com.apple.dock tilesize -integer 64; killall Dock
```
```bash
defaults write com.apple.dock size-immutable -bool yes; killall Dock
```
