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