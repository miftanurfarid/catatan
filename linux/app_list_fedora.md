sudo dnf install texlive-scheme-basic lyx octave python3-spyder python3.9 git-core htop inkscape libreoffice texstudio xournal xournalpp qpdfview-qt5 okular gimp playonlinux podman cheese

sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc

sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'

sudo dnf check-update

sudo dnf install code