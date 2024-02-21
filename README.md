# tmux
My TMUX configuration 

**UBUNTU**

## 1. Install fonts [https://github.com/ryanoasis/nerd-fonts]

```
mkdir -p ~/.local/share/fonts
cd ~/.local/share/fonts
curl -OL https://github.com/ryanoasis/nerd-fonts/releases/latest/download/JetBrainsMono.tar.xz
tar xvf JetBrainsMono.tar.xz
rm JetBrainsMono.tar.xz
cd
fc-cache -fv
fc-list | grep JetBrainsMono
```

### You can use Alacritty or Kitty terminal ###

## 2a. Install Alacritty [https://alacritty.org/config-alacritty.html]

```
sudo apt update
sudo apt upgrade
sudo add-apt-repository ppa:aslatter/ppa
sudo apt install alacritty
curl -OL https://raw.githubusercontent.com/filip-lebiecki/tmux/main/alacritty.toml
mv alacritty.toml .alacritty.toml
curl -OL https://github.com/dracula/alacritty/archive/master.zip
unzip master.zip
mv alacritty-master/dracula.toml .config
rm -rf alacritty-master/ master.zip
```

## 2b. Install Kitty [https://sw.kovidgoyal.net/kitty/]

```
sudo apt update
sudo apt upgrade
sudo apt install kitty
mkdir -p .config/kitty/
cd .config/kitty/
curl -OL https://raw.githubusercontent.com/filip-lebiecki/tmux/main/kitty.conf
```

## 3. Fish shell [https://fishshell.com/]

```
sudo apt-add-repository ppa:fish-shell/release-3
sudo apt install fish
chsh -s /usr/bin/fish
set -U fish_greeting
```

## 4. OH-MY-FISH Agnoster Theme [https://github.com/oh-my-fish/oh-my-fish]

```
curl https://raw.githubusercontent.com/oh-my-fish/oh-my-fish/master/bin/install | fish
omf install agnoster
```

## 5. Install TMUX [https://github.com/tmux-plugins/tpm]

```
sudo apt install tmux
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
curl -OL https://raw.githubusercontent.com/filip-lebiecki/tmux/main/tmux.conf
mv tmux.conf .tmux.conf
tmux
tmux source .tmux.conf
Ctrl+A Shift+I
```

## 6. LazyVIM

```
sudo add-apt-repository ppa:neovim-ppa/unstable
sudo apt install neovim
git clone https://github.com/LazyVim/starter ~/.config/nvim
rm -rf ~/.config/nvim/.git
```
