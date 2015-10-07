# My VIM environment

[Where I started](http://vimcasts.org/episodes/synchronizing-plugins-with-git-submodules-and-pathogen/)

## Installation:

    git clone git://github.com/jacobhenke/dotvim.git ~/.vim

Create symlinks:

    ln -s ~/.vim/vimrc ~/.vimrc

Switch to the `~/.vim` directory, and fetch submodules:

    cd ~/.vim
    git submodule update --init

## Install plugins as submodules

    git submodule add http://github.com/tpope/vim-fugitive.git bundle/fugitive
    git add .
    git commit -m "Install Fugitive.vim bundle as a submodule."

## Things to remember

* Move between "windows" with Ctrl+W
* Use paste mode to not auto-indent when pasting into the terminal: `:set paste` then `i` and finally `:set nopaste` when done.
    * [SO user says: I usually use](http://stackoverflow.com/questions/2514445/turning-off-auto-indent-when-pasting-text-into-vim)...
        * `:r! cat`
        * `( shift + insert )`
        * `CTRL+D`
* [NERDTree](https://github.com/scrooloose/nerdtree/blob/master/doc/NERD_tree.txt)
    * `o` - open file/directory
    * `t` - open file in new tab
    * `T` - open file in new*background* tab
    * `I` - show/hide dot files
    * :NERDTreeMirror
        Shares an existing NERD tree, from another tab, in the current tab.
        Changes made to one tree are reflected in both as they are actually the
        same buffer.
        If only one other NERD tree exists, that tree is automatically mirrored. If
        more than one exists, the script will ask which tree to mirror.
    * :NERDTreeClose
* Show whitespace characters (other than plain ' ' space) `:set list`


