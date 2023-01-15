# apt install

`sudo apt install -y texlive-full octave spyder git htop inkscape texstudio xournalpp qpdfview gimp torbrowser-launcher axel neofetch vlc telegram-desktop rclone calibre unrar python3-notebook okular neovim vim steam texmaker flatpak gnome-software-plugin-flatpak nvidia-driver-515 nvidia-dkms-515 gparted synaptic plocate bpython`

# remove minimize & maximize using gnome-tweaks

`sudo add-apt-repository universe`

`sudo apt install gnome-tweaks`

# remove games

`sudo apt purge aisleriot gnome-mahjongg gnome-mines`

# deb package install:

- vscode
- google chrome
- brave browser
- megasync
- discord
- packet tracer
- gns3

# flatpak install:

`flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo`

`flatpak install -y flathub us.zoom.Zoom io.github.shiftey.Desktop com.elsevier.MendeleyDesktop`

# snap install:

`sudo snap install superproductivity`

# disable ubuntu dock using extension manager from flatpak

`flatpak install -y flathub com.mattjakeman.ExtensionManager`

# python

`pip3 install numpy tensorflow librosa pandas seaborn opencv-python`

# cuda

https://linuxhint.com/install-cuda-ubuntu/

# add to ~/.bashrc

```
parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
    }

if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\n\[\033[01;34m\]\w\[\033[01;31m\]$(parse_git_branch)\[\033[00m\]\n> '
else
    PS1='${debian_chroot:+($debian_chroot)}\n\w$(parse_git_branch)\n> '
fi

gsettings set org.gnome.shell app-picker-layout "[]"
```
