# Update

1. `sudo pacman -Syyu`

# Install base-devel

1. `sudo pacman -S base-devel`

# Install VS Codium

1. `git clone https://aur.archlinux.org/vscodium-bin.git`

1. `makepkg -si`

# Unable to download extensions in code

1. Creating a custom `product.json` at the following location:

	1. Linux: `$XDG_CONFIG_HOME/VSCodium` or `~/.config/VSCodium`

	```
	{
		"extensionsGallery": {
			"serviceUrl": "https://marketplace.visualstudio.com/_apis/public/gallery",
			"cacheUrl": "https://vscode.blob.core.windows.net/gallery/index",
			"itemUrl": "https://marketplace.visualstudio.com/items",
			"controlUrl": "",
			"recommendationsUrl": ""
		}
	}
	```

# Install oh my zsh

1. `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

1. Konsole > Settings > Configure Konsole > Profiles > Edit > General `Command: /bin/zsh`

# Install Oh My Zsh for Root

1. `sudo ln -s $HOME/.oh-my-zsh /root/.oh-my-zsh`

1. `sudo mv /root/.zshrc /root/.zshrc.bak`

1. `sudo ln -s $HOME/.zshrc /root/.zshrc`

1. `sudo nano ~/.zshrc`

1. Add `ZSH_DISABLE_COMPFIX=true`

1. `sudo chsh -s /usr/bin/zsh root`

# Install Spaceship Theme

1. `git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1`

1. `ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"`

1. Set `ZSH_THEME="spaceship"` in your `.zshrc`.

# Install powerline fonts

1. `git clone https://github.com/powerline/fonts.git --depth=1`

1. `cd fonts`

1. `./install.sh`

1. `fc-cache -vf`

# Fix oh my zsh + powerline fonts + visual studio code (vscode) terminal settings

1. Edit file `~/.config/VSCodium/User/settings.json`

    ```
	{
		"git.autofetch": true,
		"terminal.integrated.automationShell.linux": "/bin/zsh",
		"terminal.integrated.fontFamily": "Ubuntu Mono derivative Powerline",
		"terminal.integrated.rendererType": "canvas",
		"terminal.integrated.fontSize": 12,
		"terminal.integrated.lineHeight": 1.1
	}
    ```

# Install libreoffice

1. `sudo pacman -S libreoffice-still`

# Install Telegram

1. `sudo pacman -S telegram-desktop`

# Install Rclone

1. `sudo pacman -S rclone`

# Install Texlive + Texstudion

1. `sudo pacman -S texlive-most texstudio`