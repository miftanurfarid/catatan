##### install driver

pacman -S xf86-input-wacom

systemctl restart display-manager


##### get id

xsetwacom list devices


##### config

xsetwacom set <id> mode relative

xsetwacom set <id> area -15000 0 15000 20000


##### permanent configuration

grep "Using input driver 'wacom'" /var/log/Xorg.0.log

```
[  5362.130] (II) Using input driver 'wacom' for 'Wacom One by Wacom S Pen'
[  5362.747] (II) Using input driver 'wacom' for 'Wacom One by Wacom S Pen eraser'

```

pluma /usr/share/X11/xorg.conf.d/70-wacom.conf

sesuai keluaran dari Xorg.0.log

```
Section "InputClass"
	Identifier "WACOM OPTIONS pen"
	MatchDriver "wacom"
	MatchProduct "Pen"
	NoMatchProduct "eraser"
	Option "Mode" "Relative"
	Option "TopX" "0"
	Option "TopY" "0"
	Option "BottomX" "30000"
	Option "BottomY" "20000"
	Option "CursorProx" "10"
EndSection

Section "InputClass"
	Identifier "WACOM OPTIONS eraser"
	MatchDriver "wacom"
	MatchProduct "eraser"
EndSection
```
