# terminal
Chuck's super simple settings and preferences for iTerm2.

# Get oh my zsh
I'm lazy and the new MacBooks suggest `zsh` by default instead of `bash`. Seriously, get [Oh My Zsh](https://ohmyz.sh/).

```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

# Get the ultimate vimrc
Credit to [Amix](https://github.com/amix/vimrc), simple and comfortable text editing in terminal.
```
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh
```

# Install brew.sh
What madman doesn't install [brew](https://brew.sh) to manage their package!?

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

# Setup tmux
tmux is fantastic if you need to manage multiple windows and multiple settings with minimal fuss. I've forked from [tony](http://tony.github.io/tmux-config/) but added automatic save and restore on system restart 😉.

```
git clone https://github.com/chuckwired/tmux-config.git ~/.tmux
ln -s ~/.tmux/.tmux.conf ~/.tmux.conf
```

# Personal iTerm2 profile
Get the global window hotkey using `Option + Spacebar` and convenience keys like `Option + ->` or `Shift + <-` to skip word by word within the command line.

1. Open iTerm2
1. Press `Cmd + ,` to open preferences
1. Select profiles
1. Bottom left, select `Other actions...`
1. Import JSON profiles...

You can guess the rest.

# Finally, usual packages
Just install the usual things that you'll probably need.

```
brew install tmux nvm
```