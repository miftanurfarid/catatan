https://aur.archlinux.org/packages/vmware-workstation/

https://aur.archlinux.org/packages/vmware-keymaps/

https://www.archlinux.org/packages/community/x86_64/pcsclite/


After the first installation, please:

1. install the appropriate headers package(s) for your installed kernel(s): linux-headers for default kernel, linux-lts-headers for LTS kernel...

2. Enable the services you need:

    systemctl enable vmware-networks.service : *for guest network access*

    systemctl enable vmware-usbarbitrator.service : *for connecting USB devices to guest*

    systemctl enable vmware-hostd.service : *for sharing virtual machines*

3. reboot or load vmw_vmci and vmmon kernel modules (modprobe -a vmw_vmci vmmon)
