# Fedora Spin i3WM

## things to do after fresh install
1. `echo 'fastestmirror=true' | sudo tee -a /etc/dnf/dnf.conf`
2. `echo 'max_parallel_downloads=5' | sudo tee -a /etc/dnf/dnf.conf`
3. `echo 'deltarpm=true' | sudo tee -a /etc/dnf/dnf.conf`
4. `sudo rpm -Uvh http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm`
5. `sudo dnf install -y https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm`
6. `sudo dnf upgrade -y --refresh`
7. `sudo dnf install -y texlive-scheme-full lyx octave python3-spyder htop inkscape texstudio xournalpp qpdfview-qt5 gimp texlive-IEEEtran libreoffice-Mendeley axel neofetch vlc telegram-desktop rclone calibre unrar jupyter-notebook okular texlive-babel-bahasa texlive-lipsum texlive-extarrows btrfs-assistant transmission xorg-x11-font-utils redhat-lsb-core gstreamer1-plugin-openh264 mozilla-openh264 neovim bat exa fish polybar rofi pdftk simple-scan git evince help2man arandr maim xclip xdotool google-noto-emoji-color-fonts google-noto-emoji-fonts texlive-noto-emoji trash-cli`
8. `sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc`
9. `sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'`
10. `sudo dnf check-update`
11. `sudo dnf install -y code`
12. `sudo rpm --import https://dl.google.com/linux/linux_signing_key.pub`
13. `axel -a https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm`
14. `sudo dnf install -y google-chrome-stable_current_x86_64.rpm`
15. `sudo dnf config-manager --add-repo https://brave-browser-rpm-release.s3.brave.com/x86_64/`
16. `sudo rpm --import https://brave-browser-rpm-release.s3.brave.com/brave-core.asc`
17. `sudo dnf install -y brave-browser`
18. `sudo dnf install -y https://downloads.sourceforge.net/project/mscorefonts2/rpms/msttcore-fonts-installer-2.6-1.noarch.rpm`
19. config git
  ```
  git config --global user.name "miftanurfarid"
  git config --global user.email "miftanurfarid@gmail.com"
  git config --global init.defaultBranch master
  git config --global pull.rebase true
  ```
20. in `/home/$user/.bashrc` add the following line:
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
11. copy `.config`
12. copy `/etc/hosts`
13. setting monitor using arandr
14. install `mons` from [https://github.com/Ventto/mons](https://github.com/Ventto/mons)
    1. `git clone git@github.com:Ventto/mons.git --recursive`
    2. `sudo dnf groupinstall "Development Tools"`
    3. `sudo make install`
15. copy `90-touchpad.conf` to `/etc/X11/xorg.conf.d/` to enable tap for click and natural scrolling
16. `sudo cp -v nobeep.conf /etc/modprode.d/`
17. doing `i3blocks`. this will replace `i3status`.
    1. `git clone https://github.com/Airblader/i3blocks-gaps i3blocks`
    2. `cd i3blocks`
    3. `make clean all`
    4. `sudo make install`
    5. in `~/.config/i3/config`, change `status_command i3status` into `status_command i3blocks`
    6. go to [ihttps://github.com/vivien/i3blocks-contrib](https://github.com/vivien/i3blocks-contrib)
    7. 
14. copy `/etc/selinux/config` to disable selinux

## Gruv Fedora Theme

source: [https://www.youtube.com/watch?v=kWRQoLFntQc](https://www.youtube.com/watch?v=kWRQoLFntQc)

packages list:
1. i3
2. polybar
3. alacritty

to do
1. edit `.config/i3/config`
  1. change default terminal to alacritty
  2. change close windows key to super+Q
  3. delete the bar at the bottom
  4. mkdir .config/polybar
  5. cp /etc/polybar/config.ini .config/polybar/
  6. vim .config/polybar/launch.sh
    1. read [https://github.com/polybar/polybar/wiki](https://github.com/polybar/polybar/wiki)

## Need to watch
1. [[i3] More rice maturing, quite satisfied with the Neovim config](https://www.reddit.com/r/unixporn/comments/12xcx6j/i3_more_rice_maturing_quite_satisfied_with_the/)
