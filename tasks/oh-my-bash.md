# oh my zsh

```bash
sudo apt update
sudo apt install git
sudo apt install curl
bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
bash -c "$(wget https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh -O -)"
```

---

### install locally

```bash
git clone --depth=1 https://github.com/ohmybash/oh-my-bash.git ~/backup.oh-my-bash
# all file is here
~/backup.oh-my-bash
# change name to
~/.oh-my-bash
# command for execute
vim ~/.bashrc
# add these command at the end of file
# Path to your oh-my-bash installation
export OSH="~/.oh-my-bash"

# Set name of the theme to load
OSH_THEME="font"

# Which plugins would you like to load?
plugins=(git bash-completion)

# Load oh-my-bash
source $OSH/oh-my-bash.sh
```

---

#### themes

```bash
vim ~/.zshrcbashrc

	OSH_THEM="font" g
	OSH_THEM=""    n
	OSH_THEM="fishy"   n
	OSH_THEM="fox"     n
	OSH_THEM="frisk"     g
	OSH_THEM="funky"   n
	OSH_THEM="gentoo"  n
	OSH_THEM="geoffgarside"  g
	OSH_THEM="gnzh"    n
	OSH_THEM="font"    g
	OSH_THEM="gentoo" *
	OSH_THEM="geoffgarside" ## clock
	OSH_THEM="gozilla" **
	OSH_THEM="muse" **
	OSH_THEM="robbyrussell" **
	OSH_THEM="bira" #
	OSH_THEM="obraun" ##
	OSH_THEM="avit" #
```

---

### reload

```bash
sources .bashrc
```