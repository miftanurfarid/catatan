# Downgrade package

1. `https://aur.archlinux.org/packages/downgrade/`

2. `sudo downgrade <package-name>`

3. `choose version`

4. stop after downloading finished / choose `n` for installation

5. install via pacman: `sudo pacman -S <package-name>`

# Double quote keys and @

1. 'setxkbmap -layout us'

# Google Chrome

1. `sudo pacman -S --needed base-devel git`

2. `git clone https://aur.archlinux.org/google-chrome.git`

3. `cd google-chrome`

4. `makepkg -si`
