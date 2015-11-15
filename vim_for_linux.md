# get vim ready for linux
This doc is mainly for install/compile vim and configure
it in linux.

## Install/Compile Vim with Python and other support
1. remove the vim version without python support
`
sudo apt-get remove vim vim-runtime gvim vim-tiny vim-common vim-gui-common 
`

2. install all the prerequisite libraries, including Git
`
sudo apt-get install build-dep vim 
` 

3. clone and compile vim74
```
cd ~
git clone https://github.com/vim/vim.git
cd vim
./configure --with-features=huge \
            --enable-multibyte \
            --enable-rubyinterp \
            --enable-pythoninterp \
            --with-python-config-dir=/usr/lib/python2.7/config \
            --enable-perlinterp \
            --enable-luainterp \
            --enable-gui=gtk2 --enable-cscope --prefix=/usr
make VIMRUNTIMEDIR=/usr/share/vim/vim74
sudo make install
```
4. Set vim as the default editor with `update-alternatives`
```
sudo update-alternatives --install /usr/bin/editor editor /usr/bin/vim 1
sudo update-alternatives --set editor /usr/bin/vim
sudo update-alternatives --install /usr/bin/vi vi /usr/bin/vim 1
sudo update-alternatives --set vi /usr/bin/vim
```

## Install YouCompleteMe 
This part is trying to use **Pathogen** to install the YCM package.

### Get Pathogen
use the code below to get **Pathogen** ready for use
```
mkdir -p ~/.vim/autoload ~/.vim/bundle && \
curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim
```

Add this to the vimrc:
```
execute pathogen#infect()
```

### Set an initial *vimrc*
```
execute pathogen#infect()

syntax on

filetype plugin indent on
```

and install **vim-sensible**
`
cd ~/.vim/bundle && \
git clone git://github.com/tpope/vim-sensible.git
`

### Clone and compile YCM
clone YCM to `~/.vim/bundles/`
`
cd ~/.vim/bundle && \
git clone https://github.com/Valloric/YouCompleteMe.git
`
fetch dependencies
`
cd ~/.vim/bundle/YouCompleteMe && \
git submodule update --init --recursive
`

Install development tools and CMake:
`sudo apt-get install build-essential cmake`

make sure have Python headers installed `sudo apt-get install python-dev`

Compile YCM with semantic support for C-family languages:
`cd ~/.vim/bundle/YouCompleteMe
./install.py --clang-completer --gocode-completer`

