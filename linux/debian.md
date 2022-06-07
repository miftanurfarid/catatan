sudo cp /etc/apt/sources.list /etc/apt/sources.list.backup

sudo echo "deb http://kartolo.sby.datautama.net.id/debian/ testing main contrib non-free" > /etc/apt/sources.list

sudo apt update

sudo apt upgrade

sudo reboot

sudo apt dist-upgrade

sudo reboot

sudo rm -r ~/.cache/tracker

sudo rm -r ~/.local/share/tracker

sudo apt-get install firmware-atheros

sudo reboot
