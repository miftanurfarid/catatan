sudo zypper refresh

sudo zypper update

sudo zypper install texlive-scheme-medium lyx octave spyder3 git-core htop inkscape texstudio xournal xournalpp qpdfview gimp torbrowser-launcher axel neofetch telegram-desktop playonlinux flatpak

sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc

sudo zypper addrepo https://packages.microsoft.com/yumrepos/vscode vscode

sudo zypper refresh

sudo zypper install code

wget https://dl.google.com/linux/linux_signing_key.pub

sudo rpm --import linux_signing_key.pub

wget https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm

sudo zypper install google-chrome-stable_current_x86_64.rpm

wget https://github.com/shiftkey/desktop/releases/download/release-2.9.6-linux1/GitHubDesktop-linux-2.9.6-linux1.rpm

sudo zypper install GitHubDesktop-linux-2.9.6-linux1.rpm

wget https://github.com/johannesjo/super-productivity/releases/download/v7.10.1/superProductivity-7.10.1.x86_64.rpm

sudo zypper install superProductivity-7.10.1.x86_64.rpm

flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

flatpak install flathub  us.zoom.Zoom org.onlyoffice.desktopeditors com.wps.Office com.bitwarden.desktop io.bit3.WhatsAppQT io.gitlab.librewolf-community
