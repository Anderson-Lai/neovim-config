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

### Setting up win32yank
Download win32yank [here](https://github.com/equalsraf/win32yank/releases) <br />
Extract the zip file into 'win32yank' <br />
Move 'win32yank' to C:\win32yank (the complete path to win32yank.exe should be 'C:\win32yank\win32yank.exe')

### Setting up intellisense for C/C++
```
sudo snap install ccls --classic
sudo snap install node --classic
nvim
:PlugInstall
```

### Setting up intellisense for CMake
```
nvim
:CocInstall coc-cmake 
```

### Setting up intellisense for Rust
#### First, install rust and cargo
```
curl https://sh.rustup.rs -sSf | sh 
```

Restart terminal <br />
```
nvim
:CocInstall coc-rust-analyzer
```

#### Installing rust-analyzer
```
rustup component add rust-rc
rustup component add rust-analyzer-preview
```

### Fixing git
```
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager.exe"
```
Download git for windows [here](https://git-scm.com/download/win) <br />
Git push on a repository, and follow instructions to login with browser
