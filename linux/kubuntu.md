do apt update
sudo apt upgrade
sudo apt dist-upgrade
sudo apt install -y libreoffice texstudio git flatpak lyx octave lyx octave spyder3 htop inkscape xournal qpdfview gimp torbrowser-launcher axel neofetch vlc telegram-desktop simple-scan playonlinux python3-pip python3-notebook
sudo apt-get install wget gpg
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/trusted.gpg.d/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
rm -f packages.microsoft.gpg
sudo apt install apt-transport-https
sudo apt update
sudo apt install code
wget https://github.com/shiftkey/desktop/releases/download/release-2.9.6-linux1/GitHubDesktop-linux-2.9.6-linux1.deb
sudo dpkg -i GitHubDesktop-linux-2.9.6-linux1.deb
sudo apt install --fix-broken
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
wget https://zoom.us/client/latest/zoom_amd64.deb
sudo dpkg -i zoom_amd64.deb
sudo apt install --fix-broken
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install -y org.onlyoffice.desktopeditors io.bit3.WhatsAppQT io.gitlab.librewolf-community
