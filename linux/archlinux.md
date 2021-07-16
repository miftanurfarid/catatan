# Catatan Selama Menggunakan Arch Linux

## Remove unused dependencies

1. List all orphans: `pacman -Qdt`

2. Remove them all: `pacman -Rsn $(pacman -Qdtq)`

## Downgrade package

1. `https://aur.archlinux.org/packages/downgrade/`

2. `sudo downgrade <package-name>`

3. `choose version`

4. stop after downloading finished / choose `n` for installation

5. install via pacman: `sudo pacman -S <package-name>`

## Double quote keys and @

1. 'setxkbmap -layout us'

## Google Chrome

1. `sudo pacman -S --needed base-devel git`

2. `git clone https://aur.archlinux.org/google-chrome.git`

3. `cd google-chrome`

4. `makepkg -si`

## Light Locker

1. `pacman -S xfce4-screensaver`

1. vim `/usr/bin/xflock4`

1.
    ```
    #!/bin/sh
    #
    #  xfce4
    #
    #  Copyright (C) 1999, 2003 Olivier Fourdan (fourdan@xfce.  org)
    #  Copyright (C) 2011       Guido Berhoerster (guido+xfce.  org@berhoerster.name)
    #  Copyright (C) 2011       Jarno Suni (8@iki.fi)
    #
    #  This program is free software; you can redistribute it   and/or modify
    #  it under the terms of the GNU General Public License as  published by
    #  the Free Software Foundation; either version 2 of the    License, or
    #  (at your option) any later version.
    #
    #  This program is distributed in the hope that it will be  useful,
    #  but WITHOUT ANY WARRANTY; without even the implied   warranty of
    #  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.     See the
    #  GNU General Public License for more details.
    #
    #  You should have received a copy of the GNU General   Public License
    #  along with this program; if not, write to the Free   Software
    #  Foundation, Inc., 59 Temple Place - Suite 330, Boston,   MA 02111-1307, USA.
    #

    # First test for the command set in the session's xfconf    channel
    LOCK_CMD=$(xfconf-query -c xfce4-session -p /general/   LockCommand)

    # Lock by xscreensaver or gnome-screensaver, if a   respective daemon is running
    for lock_cmd in \
        "$LOCK_CMD" \
        "xfce4-screensaver-command --lock" \
        "xscreensaver-command -lock" \
        "gnome-screensaver-command --lock"
    do
        if [ ! -z "$lock_cmd" ]; then
            $lock_cmd >/dev/null 2>&1 && exit
        fi
    done

    # else run another access locking utility, if installed
    for lock_cmd in \
      "xlock -mode blank" \
      "slock"
      do
        set -- $lock_cmd
        if command -v -- $1 >/dev/null 2>&1; then
            $lock_cmd >/dev/null 2>&1 &
    	# turn off display backlight:
    	xset dpms force off
            exit
        fi
    done

    # else access locking failed
    exit 1
    ```
1. `pamac build light-locker-settings`

1. set delay to 1 sec

## Enable emoji fonts

1. Available fonts

    Use any font from the table below, available from a variety of sources —


    **Package** | **Source** | **Font name**
    --- | --- | ---
    noto-fonts-emoji | Official / Extra | Noto Color Emoji
    ttf-twemoji | AUR | Twemoji
    otf-openmoji | AUR | OpenMoji
    ttf-joypixels | Official / Community | JoyPixels
