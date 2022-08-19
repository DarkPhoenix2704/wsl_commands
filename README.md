# Commands after installing WSL2

## Update the Package Information
``` 
sudo apt update && sudo apt upgrade -y
```
## Install necessary packages
```
sudo apt install zsh build-essential -y
```
## Install oh-my-zsh
```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
## Install powerlevel10k
```
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```
## Enable it by changing ZSH_THEME in .zshrc
```
ZSH_THEME="powerlevel10k/powerlevel10k"
```
## Install ZSH Plugins
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
## Activate Plugins by adding the line in .zshrc
```
plugins=( git zsh-syntax-highlighting zsh-autosuggestions )
```
## Configure Git
```
git config --global user.name "DarkPhoenix2704"
git config --global user.email "anbarasun123@gmail.com"
```
## Genarate SSH Key
```
mkdir ~/.ssh && cd ~/.ssh
ssh-keygen -t ed25519 -C "anbarasun123@gmail.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
ssh -T git@github.com
```
Add it in your github

## GPG Signing 
```
gpg --default-new-key-algo rsa4096 --gen-key
gpg --list-secret-keys --keyid-format=long
gpg --armor --export *****************
git config --global user.signingkey 
```
Add it to Github
## Put in top of .zshrc
```
export GPG_TTY=$(tty)
```
## Install NVM
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```
