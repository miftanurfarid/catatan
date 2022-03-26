# All in One

sudo pacman-mirrors --fasttrack && sudo pacman -Syyu

sudo pacman -S texlive-most texlive-bin texlive-lang lyx texstudio xournalpp octave libreoffice-still axel simple-scan rclone calibre inkscape gimp telegram-desktop spyder qpdfview torbrowser-launcher bitwarden code jupyterlab playonlinux

# AUR

git clone https://aur.archlinux.org/google-chrome.git

git clone https://aur.archlinux.org/github-desktop-bin.git

git clone https://aur.archlinux.org/librewolf-bin.git

for librewolf: gpg --keyserver hkp://keyserver.ubuntu.com --search-keys 031F7104E932F7BD7416E7F6D2845E1305D6E801

git clone https://aur.archlinux.org/onlyoffice-bin.git

https://aur.archlinux.org/wps-office-cn.git

makepkg -sir

# Zoom

Download from https://zoom.us/download?os=linux

sudo pacman -U zoom_x86_64.pkg.tar.xz
