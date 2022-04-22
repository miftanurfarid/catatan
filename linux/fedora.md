# Display Flickering

1. `sudo nano /etc/default/grub`

2. add `radeon.dpm=0`:

    ```
    GRUB_TIMEOUT=5
    GRUB_DISTRIBUTOR="$(sed 's, release .*$,,g' /etc/system-release)"
    GRUB_DEFAULT=saved
    GRUB_DISABLE_SUBMENU=true
    GRUB_TERMINAL_OUTPUT="console"
    GRUB_CMDLINE_LINUX="rhgb quiet radeon.dpm=0"
    GRUB_DISABLE_RECOVERY="true"
    GRUB_ENABLE_BLSCFG=true
    ```

3. `sudo grub2-mkconfig -o /etc/grub2-efi.cfg`

4. `reboot`

# Disable ksshaskpass in Fedora 34 KDE

echo 'unset SSH_ASKPASS' >> ~/.bashrc

# All in One

echo 'fastestmirror=true' | sudo tee -a /etc/dnf/dnf.conf

echo 'max_parallel_downloads=5' | sudo tee -a /etc/dnf/dnf.conf

echo 'deltarpm=true' | sudo tee -a /etc/dnf/dnf.conf

sudo rpm -Uvh http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm

sudo dnf install -y https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm

sudo dnf upgrade -y --refresh

sudo dnf check

sudo dnf autoremove

sudo dnf update

sudo reboot

sudo dnf install -y texlive-scheme-basic lyx octave python3-spyder git-core htop inkscape libreoffice texstudio xournal xournalpp qpdfview-qt5 gimp texlive-IEEEtran mendeleydesktop libreoffice-Mendeley torbrowser-launcher axel neofetch kcm_wacomtablet vlc telegram-desktop simple-scan ibus-m17n rclone calibre gnome-tweaks unrar

sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc

sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'

sudo dnf check-update

sudo dnf install code

axel -a https://dl.google.com/linux/linux_signing_key.pub

sudo rpm --import linux_signing_key.pub

axel -a https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm

sudo dnf install -y google-chrome-stable_current_x86_64.rpm

axel -a https://github.com/shiftkey/desktop/releases/download/release-2.9.6-linux1/GitHubDesktop-linux-2.9.6-linux1.rpm

sudo dnf install -y GitHubDesktop-linux-2.9.6-linux1.rpm

axel -a https://github.com/shiftkey/desktop/releases/download/release-2.9.9-linux2/GitHubDesktop-linux-2.9.9-linux2.rpm

sudo dnf install -y GitHubDesktop-linux-2.9.9-linux2.rpm

axel -a https://zoom.us/client/latest/zoom_x86_64.rpm

axel -a https://zoom.us/linux/download/pubkey

sudo rpm --import package-signing-key.pub

sudo rpm -i zoom_x86_64.rpm

bitwarden no auto-update: https://bitwarden.com/download/

wps-office no auto-update: https://www.wps.com/download/

flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

flatpak install -y flathub org.onlyoffice.desktopeditors io.gitlab.librewolf-community com.wps.Office com.bitwarden.desktop

git clone https://github.com/IamDH4/ttf-wps-fonts.git

cd ttf-wps-fonts

sudo bash install.sh

pip3 install tensorflow librosa jupyterlab seaborn pandas

sudo dnf install curl cabextract xorg-x11-font-utils fontconfig

sudo rpm -i https://downloads.sourceforge.net/project/mscorefonts2/rpms/msttcore-fonts-installer-2.6-1.noarch.rpm

sudo dnf install playonlinux
