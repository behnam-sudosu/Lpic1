# oh my zsh  

```bash
sudo apt update
sudo apt install git
sudo apt install curl
sudo apt install zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"  
```
### install locally
```bash
git clone --depth=1 https://github.com/ohmyzsh/ohmyzsh.git ~/backup.oh-my-zsh
# all file is here
~/backup.oh-my-zsh
# change name to
~/.oh-my-zsh
# command for execute
sh ~/.oh-my-zsh/tools/install.sh --unattended

```
---  

#### themes

```bash
vim ~/.zshrc

	ZSH_THEME="fino-time" g
	ZSH_THEME="fino"    n
	ZSH_THEME="fishy"   n
	ZSH_THEME="fox"     n
	ZSHy_THEME="frisk"     g
	ZSH_THEME="funky"   n
	ZSH_THEME="gentoo"  n
	ZSH_THEME="geoffgarside"  g
	ZSH_THEME="gnzh"    n
	ZSH_THEME="font"    g
	ZSH_THEME="gentoo" *
	ZSH_THEME="geoffgarside" ## clock
	ZSH_THEME="gozilla" **
	ZSH_THEME="muse" **
	ZSH_THEME="robbyrussell" **
	ZSH_THEME="bira" #
	ZSH_THEME="obraun" ##
	ZSH_THEME="avit" #
```

---  

### reload

```bash
sources .zshrc
```