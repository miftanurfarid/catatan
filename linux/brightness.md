# brightness reset after reboot (for init system, not systemd)

1. check using command `ps -p 1 -o comm=`

2. if it show `init`:

    1. sudo nano `/etc/rc.local`

    2. `echo 50 > /sys/class/backlight/amdgpu_bl0/brightness`

3. if it show 'systemd'

    1. `sudo nano /etc/default/grub`

    2. add parameter `acpi_backlight=video` or `acpi_backlight=vendor` or `acpi_backlight=native` then save

    3. `sudo update-grub`
