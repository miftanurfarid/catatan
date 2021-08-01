# Display Flickering

1. `sudo nano /etc/default/grub`

2. add `radeon.dpm=0`:

    ```
    GRUB_TIMEOUT=5
    GRUB_DISTRIBUTOR="$(sed 's, release .*$,,g' /etc/system-release)"
    GRUB_DEFAULT=saved
    GRUB_DISABLE_SUBMENU=true
    GRUB_TERMINAL_OUTPUT="console"
    GRUB_CMDLINE_LINUX="rhgb quiet radeon.dpm=0"
    GRUB_DISABLE_RECOVERY="true"
    GRUB_ENABLE_BLSCFG=true
    ```

3. `sudo grub2-mkconfig -o /etc/grub2-efi.cfg`

4. `reboot`


# Enable RPM Fusion

1. To enable the Free repository, use:
    
    ```
    sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
    ```

2. Optionally, enable the Nonfree repository:

    ```
    sudo dnf install https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
    ```

# Disable ksshaskpass in Fedora 34 KDE

1. add `unset SSH_ASKPASS` in `.bashrc`