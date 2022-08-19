# Commands after installing WSL2

## Update the Package Information
``` 
sudo apt update && sudo apt upgrade -y
```
## Install necessary packages
```
sudo apt install zsh build-essential
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
```
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
## Activate Plugins by adding the line in .zshrc
```
plugins=( git zsh-syntax-highlighting zsh-autosuggestions )
```
