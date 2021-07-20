# Spyder is not starting in arch linux

1. seems decorator (python-decorator) is too new, there is v5.0.9 in the repository now

2. You can download the PKGBUILD for python-decorator 4.4.2 here:

	`https://github.com/archlinux/svntogit-community/tree/36ffce0448fd34612011d10fdd75169a0dd384c9/trunk`

3.  use `makepkg` to build the package and use `sudo pacman -U` to install it.
