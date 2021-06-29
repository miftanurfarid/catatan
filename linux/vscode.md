# VSCode Terminal Font Fix on Arch Linux

1. Download from AUR

	`https://aur.archlinux.org/packages/nerd-fonts-complete/`

2. Fix PKGBUILD to make download resumeable

	`https://github.com/ryanoasis/nerd-fonts/issues/274#issuecomment-605657287`

3. `makepkg -sir`
