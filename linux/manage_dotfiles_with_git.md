# How to manage your dotfiles with git

## Getting started

1. Create a `.dotfiles` folder, which we'll use to track your dotfiles
    
    ```
    git init --bare $HOME/.dotfiles
    ```

2. Create an alias `dotfiles` so you don't need to type it all over again

    ```
    alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
    ```

3. set git status to hide untracked files

    ```
    dotfiles config --local status.showUntrackedFiles no
    ```

4. add the alias to `.bashrc` (or `.zshrc`) so you can use it later

    ```
    echo "alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'" >> $HOME/.bashrc
    ```

## Usage

Now you can use regular git commands such as:

```
dotfiles status
dotfiles add .vimrc
dotfiles commit -m "Add vimrc"
dotfiles add .bashrc
dotfiles commit -m "Add bashrc"
dotfiles push
```

Nice, right? Now if you're moving to a virgin system…

## Setup environment in a new computer

Make sure to have git installed, then:

1. clone your github repository

    ```
    git clone --bare git@github.com:miftanurfarid/.dotfiles.git $HOME/.dotfiles
    ```

2. define the alias in the current shell scope
    ```
    alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
    ```
3. checkout the actual content from the git repository to your `$HOME`
    ```
    dotfiles checkout
    ```
