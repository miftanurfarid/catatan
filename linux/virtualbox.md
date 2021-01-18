## VirtualBox “Kernel driver not installed” error despite running /sbin/vboxconfig

modprobe -a vboxdrv


##  Disable and enable VirtualBox guest-host time sync

### From Guest

#### Disable time sync from guest

/etc/init.d/vboxadd-service stop

#### Enable time sync from guest

/etc/init.d/vboxadd-service start

### From Host

#### Disable time sync from host

VBoxManage setextradata "<vm-name>" VBoxInternal/Devices/VMMDev/0/Config/GetHostTimeDisabled 1

Restart VM

#### Enable time sync from host

VBoxManage setextradata "<vm-name>" VBoxInternal/Devices/VMMDev/0/Config/GetHostTimeDisabled 0

Restart VM