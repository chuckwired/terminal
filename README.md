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
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
tmux source ~/.tmux.conf
```

# Finally, usual packages
Just install the usual things that you'll probably need.

```
brew install tmux nvm
```
# TLDR;

Copy/paste this
```
# get ohmyzsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# get awesome vim
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh

# get brew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

# gitconfig
cp .gitconfig ~/.gitconfig

# bash_profile
cp .bash_profile.chuck ~/.bash_profile
source ~/.bash_profile

# install packages
brew install tmux nvm

# setup tmux
git clone https://github.com/chuckwired/tmux-config.git ~/.tmux
ln -s ~/.tmux/.tmux.conf ~/.tmux.conf
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
tmux source ~/.tmux.conf
```

## Updating plugins, configs, and tools
If moving to a new Mac, or haven't done it for a while, it's worth routinely updating upstreams for plugs and configs.

```
# Update awesome vim
cd ~/.vim_runtime && git fetch && git pull && sh ~/.vim_runtime/install_awesome_vimrc.sh && popd

# Update vim plugins
cd ~/.vim/plugged; for i in $(ls); do cd $i && git fetch && git pull && cd ..; done

# Reload vim config, and zsh config
source ~/.vimrc; source ~/.zshrc

# Finally, update via brew
brew update
```
