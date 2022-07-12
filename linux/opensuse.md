# OpenSUSE Tumbleweed

1. Install Usefull Package

   - `sudo zypper refresh`

   - `sudo zypper update`

   - `sudo zypper install texlive-scheme-medium lyx octave spyder git-core htop inkscape texstudio xournalpp qpdfview gimp torbrowser-launcher axel neofetch telegram-desktop flatpak 7zip PlayOnLinux`

1. VS Code

   - `sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc`

   - `sudo zypper addrepo https://packages.microsoft.com/yumrepos/vscode vscode`

   - `sudo zypper refresh`

   - `sudo zypper install code`

1. Google Chrome

   - `wget https://dl.google.com/linux/linux_signing_key.pub`

   - `sudo rpm --import linux_signing_key.pub`

   - `wget https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm`

   - `sudo zypper install google-chrome-stable_current_x86_64.rpm`

1. Install Github Desktop
   
   1. RPM File
   
   - `wget https://github.com/shiftkey/desktop/releases/download/release-3.0.2-linux1/GitHubDesktop-linux-3.0.2-linux1.rpm`

   - `sudo zypper install GitHubDesktop-linux-3.0.2-linux1.rpm`

   2. Repo
  
   - `sudo rpm --import https://mirror.mwt.me/ghd/gpgkey`
		
   - `sudo sh -c 'echo -e "[shiftkey]\nname=GitHub Desktop\nbaseurl=https://mirror.mwt.me/ghd/rpm\nenabled=1\ngpgcheck=0\nrepo_gpgcheck=1\ngpgkey=https://mirror.mwt.me/ghd/gpgkey" > /etc/zypp/repos.d/shiftkey-desktop.repo'`
		
   - `sudo zypper ref && sudo zypper in github-desktop`

1. SuperProductivity

   - `wget https://github.com/johannesjo/super-productivity/releases/download/v7.10.1/superProductivity-7.10.1.x86_64.rpm`

   - `sudo zypper install superProductivity-7.10.1.x86_64.rpm`

1. Packman Repo

   - `sudo zypper ar -cfp 90 https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Tumbleweed/ packman`

   - `sudo zypper refresh`

   - `sudo zypper install x264 libx265-199 libx264-161 ffmpeg gstreamer-plugins-bad gstreamer-plugins-ugly gstreamer-plugins-libav`

1. Brave Browser

   - `sudo rpm --import https://brave-browser-rpm-release.s3.brave.com/brave-core.asc`

   - `sudo zypper addrepo --refresh https://brave-browser-rpm-release.s3.brave.com/x86_64/ brave-browser`

   - `sudo zypper refresh`
  
   - `sudo zypper install brave-browser`
  
1. Sort Application Gnome

   - `gsettings set org.gnome.shell app-picker-layout "[]"`

1. Flatpak

   - `flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo`

   - `flatpak install flathub us.zoom.Zoom org.onlyoffice.desktopeditors com.wps.Office com.bitwarden.desktop io.gitlab.librewolf-community`
