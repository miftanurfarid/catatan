1. `echo 'fastestmirror=true' | sudo tee -a /etc/dnf/dnf.conf`
2. `echo 'max_parallel_downloads=5' | sudo tee -a /etc/dnf/dnf.conf`
3. `echo 'deltarpm=true' | sudo tee -a /etc/dnf/dnf.conf`
4. `sudo rpm -Uvh http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm`
5. `sudo dnf install -y https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm`
6. `sudo dnf upgrade -y --refresh`
7. `sudo dnf install -y texlive-scheme-full lyx octave python3-spyder htop inkscape texstudio xournalpp qpdfview-qt5 gimp texlive-IEEEtran libreoffice-Mendeley axel neofetch vlc telegram-desktop rclone calibre unrar jupyter-notebook okular texlive-babel-bahasa texlive-lipsum texlive-extarrows btrfs-assistant transmission xorg-x11-font-utils redhat-lsb-core gstreamer1-plugin-openh264 mozilla-openh264 neovim bat exa fish polybar rofi pdftk simple-scan git`
8. config git
  ```
  git config --global user.name "miftanurfarid"
  git config --global user.email "miftanurfarid@gmail.com"
  git config --global init.defaultBranch master
  ```
9. in `/home/$user/.bashrc` add the following line:
  ```
  parse_git_branch() {
       git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
   }
 
  export PS1="\n\[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\]\n> "
  ```
10. in `/home/root/.bashrc` add the following line:
  ```
  parse_git_branch() {
       git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
   }
 
  export PS1="\n\[\033[0;31m\][\u]\[\033[0;37m\]:\[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\]\n> "
  ```