<<<<<<< HEAD
1. `sudo zypper refresh`

1. `sudo zypper update`

1. `sudo zypper ar -cfp 90 https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Tumbleweed/ packman`

1. `sudo zypper dup --from packman --allow-vendor-change`

1. `sudo zypper install zsh git git-cola neofetch telegram-desktop rclone rclone-bash-completion rclone-zsh-completion octave texstudio`

1. [https://miftanurfarid.github.io/oh-my-zsh-spaceship-powerline-vscodium/](https://miftanurfarid.github.io/oh-my-zsh-spaceship-powerline-vscodium/)

1. Visual Studio Code

    ```
    sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
    sudo zypper addrepo https://packages.microsoft.com/yumrepos/vscode vscode
    sudo zypper refresh
    sudo zypper install code
    ```

    ```
    {
        "terminal.integrated.defaultProfile.linux": "zsh",
        "git.autofetch": true,
        "terminal.integrated.automationShell.linux": "/bin/zsh",
        "terminal.integrated.fontFamily": "Roboto Mono for Powerline",
        "terminal.integrated.rendererType": "canvas",
        "terminal.integrated.fontSize": 12,
        "terminal.integrated.lineHeight": 1.1
    }
    ```
=======
1. update local repo: `sudo zypper refresh`

1. update system: `sudo zypper update`

1. install git: `sudo zypper install git`


1. add Packman:

    ```
    sudo zypper ar -cfp 90 https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Tumbleweed/ packman

    sudo zypper dup --from packman --allow-vendor-change
    ```

1. Install Multimedia Codecs

>>>>>>> 50bbd435fe40cee02981c21dc40f79c9a8952ee2
