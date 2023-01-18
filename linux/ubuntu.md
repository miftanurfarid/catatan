# apt install

`sudo apt install -y texlive-full octave spyder git htop inkscape texstudio xournalpp qpdfview gimp torbrowser-launcher axel neofetch vlc telegram-desktop rclone calibre unrar python3-notebook okular neovim vim steam texmaker flatpak gnome-software-plugin-flatpak nvidia-driver-515 nvidia-dkms-515 gparted synaptic plocate bpython`

# remove minimize & maximize using gnome-tweaks

`sudo add-apt-repository universe`

`sudo apt install gnome-tweaks`

# remove games

`sudo apt purge aisleriot gnome-mahjongg gnome-mines`

# flatpak install:

`flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo`

`flatpak install -y flathub us.zoom.Zoom io.github.shiftey.Desktop`

# snap install:

`sudo snap install superproductivity`

# disable ubuntu dock using extension manager from flatpak

`flatpak install -y flathub com.mattjakeman.ExtensionManager`

1. clipboard

2. tray

3. shell-theme


# change ~/.bashrc

```
parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
    }

if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\n\[\033[01;34m\]\w\[\033[01;31m\] $(parse_git_branch)\[\033[00m\]:\n> '
else
    PS1='${debian_chroot:+($debian_chroot)}\n\w $(parse_git_branch):\n> '
fi
```

# add to ~/.bashrc

```
gsettings set org.gnome.shell app-picker-layout "[]"
```

# deb package install:

- vscode
- google chrome
- discord
- packet tracer
- megasync

# install brave browser
```
sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update

sudo apt install brave-browser
```

# install gns3
```
sudo add-apt-repository ppa:gns3/ppa
sudo apt update
sudo apt install -y gns3-gui gns3-server
```

for IOU support

```
sudo dpkg --add-architecture i386
sudo apt update
sudo apt install gns3-iou
```

# install matlab

- download iso
- use academic account

# install mendeley

`axel -a -n 2 https://desktop-download.mendeley.com/download/apt/pool/main/m/mendeleydesktop/mendeleydesktop_1.19.8-stable_amd64.deb`

`sudo apt install gconf2`

`sudo dpkg --ignore-depends=python -i mendeleydesktop_1.19.8-stable_amd64.deb`

`flatpak install -y flathub com.elsevier.MendeleyDesktop`

# python

`pip3 install numpy tensorflow librosa pandas seaborn opencv-python`

# cuda

https://linuxhint.com/install-cuda-ubuntu/

