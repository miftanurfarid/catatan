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

sudo dnf install -y texlive-scheme-basic lyx octave python3-spyder git-core htop inkscape libreoffice texstudio xournal xournalpp qpdfview-qt5 gimp texlive-IEEEtran mendeleydesktop libreoffice-Mendeley torbrowser-launcher axel neofetch kcm_wacomtablet vlc telegram-desktop simple-scan ibus-m17n rclone calibre gnome-tweaks unrar jupyter-notebook okular git-cola ffmpeg aria2 texlive-babel-bahasa texlive-lipsum texlive-extarrows btrfs-assistant transmission cabextract xorg-x11-font-utils redhat-lsb-core gstreamer1-plugin-openh264 mozilla-openh264 discord

sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc

sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'

sudo dnf check-update

sudo dnf install -y code

sudo rpm --import https://dl.google.com/linux/linux_signing_key.pub

axel -a https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm

sudo dnf install -y google-chrome-stable_current_x86_64.rpm

axel -a https://github.com/shiftkey/desktop/releases/download/release-3.0.6-linux1/GitHubDesktop-linux-3.0.6-linux1.rpm

sudo dnf install -y GitHubDesktop-linux-3.0.6-linux1.rpm

axel -a https://zoom.us/client/latest/zoom_x86_64.rpm

axel -a https://zoom.us/linux/download/pubkey -o package-signing-key.pub 

sudo rpm --import package-signing-key.pub

sudo dnf install -y zoom_x86_64.rpm

sudo dnf config-manager --add-repo https://brave-browser-rpm-release.s3.brave.com/x86_64/

sudo rpm --import https://brave-browser-rpm-release.s3.brave.com/brave-core.asc

sudo dnf install -y brave-browser

flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

flatpak install -y flathub com.mattjakeman.ExtensionManager

axel -a https://github.com/johannesjo/super-productivity/releases/download/v7.12.0/superProductivity-7.12.0.x86_64.rpm

sudo dnf install -y superProductivity-7.12.0.x86_64.rpm

sudo dnf install -y https://downloads.sourceforge.net/project/mscorefonts2/rpms/msttcore-fonts-installer-2.6-1.noarch.rpm

sudo dnf install -y playonlinux

gsettings set org.gnome.shell app-picker-layout "[]"

pip install tensorflow

pip install librosa

pip install seaborn

pip install pandas

pip install PyPDF2

pip install debugpy

pip install nltk

bitwarden no auto-update: https://bitwarden.com/download/

wps-office no auto-update: https://www.wps.com/download/

git clone https://github.com/IamDH4/ttf-wps-fonts.git

cd ttf-wps-fonts

sudo bash install.sh

flatpak install -y flathub org.onlyoffice.desktopeditors io.gitlab.librewolf-community com.wps.Office com.bitwarden.desktop
