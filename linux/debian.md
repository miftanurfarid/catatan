# Masalah bluetooth di laptop asus:

sudo apt-get install firmware-atheros

sudo reboot

# Masalah missing firmware pc vostro prodi

sudo apt install firmware-realtek

sudo apt install firmware-linux

# Install beberapa package 

sudo apt install git texstudio lyx texlive-lang-all xournal okular calibre qpdfview spyder jupyter-notebook octave octave-signal telegram-desktop inkscape gimp htop rclone neofetch axel vlc simple-scan torbrowser-launcher playonlinux flatpak

# Upgrade Debian Stable ke Debian Testing

sudo cp /etc/apt/sources.list /etc/apt/sources.list.backup

sudo echo "deb http://kartolo.sby.datautama.net.id/debian/ testing main contrib non-free" > /etc/apt/sources.list

sudo apt update

sudo apt upgrade

sudo reboot

sudo apt dist-upgrade

sudo reboot

sudo rm -r ~/.cache/tracker

sudo rm -r ~/.local/share/tracker
