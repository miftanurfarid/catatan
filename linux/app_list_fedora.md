sudo dnf install texlive-scheme-basic lyx octave python3-spyder python3.9 git-core htop inkscape libreoffice texstudio xournal xournalpp qpdfview-qt5 okular gimp playonlinux podman cheese texlive-IEEEtran

sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc

sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'

sudo dnf check-update

sudo dnf install code

wget https://dl.google.com/linux/linux_signing_key.pub

sudo rpm --import linux_signing_key.pub

wget https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm

sudo dnf install google-chrome-stable_current_x86_64.rpm
