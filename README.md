#gatekeeper-unquarantine
tiny bash script to remove quarantine attribute from a particular application aka resolves mac's gatekeeper issues aka `application is damaged and cant be opened` messages that also shorthands `sudo xattr -r -d com.apple.quarantine /Applications/APPNAME.app` into `sudo unq APPNAME` which is basically 75% less characters yay

###installation
1. wonder if installing this is worth typing 75% less characters
2. create a directory to store the script => clone this repo => turn script into an executable => add to $PATH env variable
3. realise i only made this repo to acquaint myself w git

###actual installation
```
sudo mkdir -p /usr/local/lib/scripts/gatekeeper-unquarantine && cd /usr/local/lib/scripts/gatekeeper-unquarantine
git clone https://github.com/satin/gatekeeper-unquarantine.git .
chmod +x unq
ln -s /usr/local/lib/scripts/gatekeeper-unquarantine/unq /usr/local/bin
source ~/.bash_profile
```
note: os x terminal.app calls for `.bash_profile` and `.profile` instead of `.bashrc`

###to uninstall
```
sudo rm /usr/local/lib/scripts/gatekeeper-unquarantine
```