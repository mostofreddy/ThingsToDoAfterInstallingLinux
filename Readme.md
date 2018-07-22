# Things to do after installing Ubuntu

## Update & Upgrade

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
sudo apt-get install linux-headers-`uname -r`
```

## Basic compilation

```
sudo apt-get install build-essential
sudo apt-get install automake make cmake libtool autoconf
```

## Utils

```
sudo apt-get install vim terminator curl ssh rar unrar zip unzip
sudo update-alternatives --config editor
```

## Codecs

```
sudo apt-get install ubuntu-restricted-extras
```

## Gimp

```
sudo apt-get install gimp gimp-data gimp-plugin-registry gimp-data-extras
```

## Gnome

```
sudo apt-get install gnome-tweak-tool gnome-shell-extensions
```

## Browsers

### Chrome

```
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
sudo apt-get update
sudo apt-get install google-chrome-stable

if [[ $(getconf LONG_BIT) = "64" ]]
then
    echo "64bit Detected" &&
    echo "Installing Google Chrome" &&
    wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb &&
    sudo dpkg -i google-chrome-stable_current_amd64.deb &&
    rm -f google-chrome-stable_current_amd64.deb
else
    echo "32bit Detected" &&
    echo "Installing Google Chrome" &&
    wget https://dl.google.com/linux/direct/google-chrome-stable_current_i386.deb &&
    sudo dpkg -i google-chrome-stable_current_i386.deb &&
    rm -f google-chrome-stable_current_i386.deb
fi
```

## Java

```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
sudo update-java-alternatives -s java-8-oracle
```

## Flash

```
sudo apt-get install flashplugin-installer
```

## Git

```
sudo apt-get install git-core
git config --global user.name "My name"
git config --global user.email "myemail@mail.com"
git config --global color.ui true
git config --global credential.helper cache
```

[Generar ssh para github & gitlab](https://help.github.com/articles/generating-ssh-keys). Luego de agregar las keys comprobar:

```
ssh -T git@github.com
```

## Windows fonts

```
sudo apt-get install ttf-mscorefonts-installer
sudo fc-cache
```

# Optimization

### preload

```
sudo apt-get install preload
```

### TLP

```
sudo add-apt-repository ppa:linrunner/tlp
sudo apt-get update
sudo apt-get upgrade
```

## UI

### Icons

```
sudo add-apt-repository ppa:papirus/papirus
sudo apt-get update
sudo apt-get install papirus-icon-theme
```
## Clean up

```
sudo apt-get -f install
sudo apt-get autoremove
sudo apt-get -y autoclean
sudo apt-get -y clean
```
