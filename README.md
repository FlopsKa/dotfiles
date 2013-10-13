# flopska/dotfiles #

## Install zsh ##
    $ sudo apt-get install zsh
    $ chsh
        /bin/zsh

## Install oh-my-zsh ##
    $ curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh 
    $ git clone https://github.com:flopska/dotfiles.git
    $ cd dotfiles
    $ ln -s $(pwd)/zsh/flopska.zsh-theme ~/.oh-my-zsh/themes/flopska.zsh-theme
    $ ln -s $(pwd)/zsh/zshrc ~/.zshrc

## Set colors in terminal ##
    $ curl -L https://raw.github.com/maksimr/dotfiles/master/gnome-terminal-themes/molokai.sh | sh 

## Compile vim with GUI and Ruby ##
    $ sudo apt-get install libncurses5-dev libgnome2-dev libgnomeui-dev \
      libgtk2.0-dev libatk1.0-dev libbonoboui2-dev \
      libcairo2-dev libx11-dev libxpm-dev libxt-dev mercurial ruby1.9.1 ruby1.9.1-dev
    $ cd ~/Downloads
    $ hg clone https://vim.googlecode.com/hg/ vim
    $ cd vim/src 
    $ ./configure --with-features=huge --enable-gui=gnome2 --enable-rubyinterp 
    $ make; sudo make install

## Install vim files ##

Download the files using git

    $ git clone https://github.com/flopska/dotfiles.git
    $ cd dotfiles
    $ git submodule init
    $ git submodule update

Creat dotfile symlinks

    $ stow --target=$HOME vim		// to create .vim and .vimrc symlinks in ~

Compile command-t

    $ cd ~/.vim/bundle/command-t/ruby/command-t
    $ ruby extconf.rb
    $ make

Enjoy
