### Installing Neovim on wsl (ubuntu)
```
cd ~
sudo snap install nvim --classic
sudo ln -s ~/snap/nvim nvim
```

### Setting up Neovim Plugins
```
curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
mkdir ~/.config
```

### Fetching Neovim configs
```
cd ~/.config
git clone https://github.com/Anderson-Lai/neovim-config.git
mv neovim-config nvim
```

### Setting up intellisense for C/C++
```
sudo snap install ccls --classic
sudo snap install node --classic
nvim
:PlugInstall
```

### Fixing git
```
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager.exe"
```
download git for windows [here](https://git-scm.com/download/win) <br />
git push on a repository, and follow instructions to login with browser
