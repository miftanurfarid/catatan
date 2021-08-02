1. update local repo: `sudo zypper refresh`

1. update system: `sudo zypper update`

1. install git: `sudo zypper install git`


1. add Packman:

    ```
    sudo zypper ar -cfp 90 https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Tumbleweed/ packman

    sudo zypper dup --from packman --allow-vendor-change
    ```

1. Install Multimedia Codecs

