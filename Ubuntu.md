# Things to do after installing Ubuntu

Tested in Ubuntu 14.04 & 14.10

## Update & Upgrade

    sudo apt-get update
    sudo apt-get upgrade
    sudo apt-get dist-upgrade
    sudo apt-get install linux-headers-`uname -r`

## Basic compilation

    sudo apt-get install build-essential
    sudo apt-get install automake make cmake libtool autoconf

---

## Terminal

### Install editor

    sudo apt-get install vim

### Console

    sudo apt-get install terminator

---


## Media / Video / Images

### Codecs

    echo 'deb http://download.videolan.org/pub/debian/stable/ /' | sudo tee -a /etc/apt/sources.list.d/libdvdcss.list && echo 'deb-src http://download.videolan.org/pub/debian/stable/ /' | sudo tee -a /etc/apt/sources.list.d/libdvdcss.list && wget -O - http://download.videolan.org/pub/debian/videolan-apt.asc|sudo apt-key add -
    sudo apt-get install libxine1-ffmpeg mencoder flac faac faad sox ffmpeg2theora
    sudo apt-get install libmpeg2-4 uudeview libmpeg3-1 mpeg3-utils mpegdemux liba52-dev
    sudo apt-get install mpeg2dec vorbis-tools id3v2 mpg321 mpg123 libflac++6 totem-mozilla
    sudo apt-get install icedax lame libmad0 libjpeg-progs libdvdcss2 libdvdread4
    sudo apt-get install libdvdnav4 libswscale-extra-2
    sudo apt-get install ubuntu-restricted-extras
    sudo /usr/share/doc/libdvdread4/install-css.sh

### Extract and compress files

    sudo apt-get install rar unrar zip unzip

### Gimp

    sudo apt-get install gimp gimp-data gimp-plugin-registry gimp-data-extras

### VLC

    sudo add-apt-repository ppa:videolan/stable-daily
    sudo apt-get update
    sudo apt-get install vlc

### OpenShot

    sudo add-apt-repository ppa:openshot.developers/ppa
    sudo apt-get update
    sudo apt-get install openshot openshot-doc

### Digicam

    sudo apt-get install digikam

---

## Torrents

### Deluge

    sudo apt-get install deluge

---

## Gnome

### Gnome3

    sudo add-apt-repository -y ppa:gnome3-team/gnome3
    sudo apt-get install gnome-shell gnome-tweak-tool gnome-shell-extensions

---

## Browsers

### Chrome

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

---

## Messengers

    sudo apt-get install pidgin
    sudo apt-get install amsn
    sudo apt-get install skype

---

## Java

    sudo add-apt-repository ppa:webupd8team/java
    sudo apt-get update
    sudo apt-get install oracle-java8-installer
    sudo update-java-alternatives -s java-8-oracle

## Flash

    sudo apt-get install flashplugin-installer

---

## Configuradores

### Ubuntu tweak

    sudo add-apt-repository ppa:tualatrix/ppa
    sudo apt install ubuntu-tweak

### dconf

    sudo apt install dconf-tools

### bleachbit

    sudo apt-get install bleachbit

---

## Repositories

### Subversion

    sudo apt-get install subversion
    sudo apt-get install colordiff

### Git

    sudo apt-get install git-core
    git config --global user.name "My name"
    git config --global user.email "myemail@mail.com"
    git config --global color.ui true
    git config --global credential.helper cache

[Generar ssh para github & gitlab](https://help.github.com/articles/generating-ssh-keys). Luego de agregar las keys comprobar:

    ssh -T git@github.com

---

## Extras & Miscellaneous

## Windows fonts

    sudo apt-get install ttf-mscorefonts-installer
    sudo fc-cache

## Optimizations

    sudo apt-get remove unity-lens-music
    sudo apt-get autoremove unity-scope-musicstores
    sudo mv /usr/bin/bluetooth-applet /usr/bin/bluetooth-applet-old
    sudo apt-get remove deja-dup
    sudo apt-get autoremove gnome-online-accounts
    sudo apt-get install preload

### Web cam software

    sudo apt-get install cheese

### FTP

    sudo apt-get install filezilla

## Others

    sudo apt-get install curl
    sudo apt-get install ssh
    sudo apt-get install vlc
    sudo apt-get install terminator
    sudo apt-get install filezilla

---

## Clean up

    sudo apt-get -f install
    sudo apt-get autoremove
    sudo apt-get -y autoclean
    sudo apt-get -y clean
