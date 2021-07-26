# brightness reset after reboot (for init system, not systemd)

1. check using command `ps -p 1 -o comm=`

2. if it show `init`, continue

3. 

3. sudo nano `/etc/rc.local`

4. `echo 50 > /sys/class/backlight/amdgpu_bl0/brightness`