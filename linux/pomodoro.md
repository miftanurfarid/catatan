# Pomodoro Timer

1. `sudo apt-get install autopoint automake autotools-dev autoconf libtool autoconf-archive gettext valac pkg-config desktop-file-utils appstream-util libappstream-glib-dev libglib2.0-dev gsettings-desktop-schemas-dev gobject-introspection libgirepository1.0-dev libsqlite3-dev libgom-1.0-dev libgstreamer1.0-dev libgtk-3-dev libcanberra-dev libpeas-dev libappindicator3-dev`

2. `git clone -b gnome-3.34 https://github.com/codito/gnome-pomodoro.git`

3. `cd gnome-pomodoro`

4. `./autogen.sh --prefix=/usr --datadir=/usr/share`

5. `make`

6. `sudo make install`
