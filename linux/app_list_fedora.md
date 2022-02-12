echo 'fastestmirror=true' | sudo tee -a /etc/dnf/dnf.conf

echo 'max_parallel_downloads=5' | sudo tee -a /etc/dnf/dnf.conf

echo 'deltarpm=true' | sudo tee -a /etc/dnf/dnf.conf

sudo rpm -Uvh http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm

sudo dnf install https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm

sudo dnf upgrade --refresh

sudo dnf check

sudo dnf autoremove

sudo dnf update

sudo reboot

sudo dnf install texlive-scheme-basic lyx octave python3-spyder python3.9 git-core htop inkscape libreoffice texstudio xournal xournalpp qpdfview-qt5 okular gimp playonlinux podman texlive-IEEEtran mendeleydesktop libreoffice-Mendeley torbrowser-launcher

sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc

sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'

sudo dnf check-update

sudo dnf install code

wget https://dl.google.com/linux/linux_signing_key.pub

sudo rpm --import linux_signing_key.pub

wget https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm

sudo dnf install google-chrome-stable_current_x86_64.rpm

flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo flatpak update

flatpak install flathub io.github.shiftey.Desktop us.zoom.Zoom org.onlyoffice.desktopeditors com.wps.Office com.bitwarden.desktop

pip install tensorflow librosa jupyterlab
