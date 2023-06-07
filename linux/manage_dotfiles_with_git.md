# How to manage your dotfiles with git

## Getting started

1. Create a `.dotfiles` folder, which we'll use to track your dotfiles
    
    `git init --bare $HOME/.dotfiles`

2. Create an alias `dotfiles` so you don't need to type it all over again

    `alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'`

3. set git status to hide untracked files

    `dotfiles config --local status.showUntrackedFiles no`

4. add the alias to `.bashrc` (or `.zshrc`) so you can use it later

    `echo "alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'" >> $HOME/.bashrc`
