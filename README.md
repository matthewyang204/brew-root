# brew-root
 A pre-modified brew.sh that allows running Homebrew as root on Macs

Please note that this only works on Macs, not Linux

Installation:

First, clone this repository to /opt/matthewyang/brew-root as root

For Apple Silicon Homebrew users, add this to your shell configuration file:
```
alias brew='cp /opt/matthewyang/brew-root/brew.sh /opt/homebrew/Library/Homebrew/brew.sh; /opt/homebrew/bin/brew'
```

For Intel Homebrew users, add this instead:
```
alias brew='cp /opt/matthewyang/brew-root/brew.sh /usr/local/Homebrew/Library/Homebrew/brew.sh; /usr/local/Homebrew/bin/brew'
```

-------------
Here's how to restore your original non-root homebrew:

Apple Silicon:
- replace the root homebrew entry in .zshrc:
```
alias brew='/opt/homebrew/bin/brew'
```
- run this to reset homebrew permissions:
```
sudo chown -R [yourusername] ~/Library/Caches/Homebrew
```

Intel Silicon:
- replace the root homebrew entry in .zshrc:
```
alias brew='/usr/local/homebrew/bin/brew'
```
- run this to reset homebrew permissions:
```
sudo chown -R [yourusername] ~/Library/Caches/Homebrew
```

After changing the stuff, restore homebrew by running `brew update` and then `brew upgrade` to reset the brew.sh file