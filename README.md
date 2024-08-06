### Installing Neovim on Ubuntu
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
sudo snapp install node --classic
nvim
:PlugInstall
```
