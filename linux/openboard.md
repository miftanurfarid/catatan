##### install driver
pacman -S xf86-input-wacom
systemctl restart display-manager

##### configuration
xsetwacom list devices  // get id
xsetwacom set <id> mode relative
xsetwacom set <id>
##### permanent configuration
