# Download
This is a setup for the **gvim** in windows, which also some hint when it is used inside ANSYS network.

So first of all, you cannot directly download it from the FTP server at vim.org from ANSYS network, a mirror is needed, try [download gvim link](http://vim.mirror.fr/). The .exe file should be a good choice if you don't really want a portable version.

# Pre-install
Before install gvim, make sure python is installed and updated, most packages still only support python 2 and 32 bits, so verison > python 2.7 and 32 bits are prefered, make sure python.dll is in the system path (environment variable PATH). Python 3's python.dll is in the **Dlls** folder.

# Install
Install gvim...

## Install pathogen
pathogen.vim is used to manage the `runtimepath`, it make install plugins and runtime files in their own private directories easy. 

1. To install pathogen.vim, just go to [github pathogen](https://github.com/tpope/vim-pathogen/blob/master/autoload/pathogen.vim), create a text file under vim/vim74/autoload, name as pathogen.vim and paste the content there. However, it is also a good idea to clone the repository and copy the file to the autoload location, in this way, you can also keep the pathogen updated as you want.

2. Create a folder  named `bundle` under \Vim\vimfiles\, in which, you can clone the plugins into it.

3. In the \_vimrc file, enter

>let g:pathogen_disabled = ["vim-easytags","YouCompleteMe"]

> execute pathogen#infect()

> execute pathogen#helptags()

> syntax on

> filetype on

> filetype plugin indent on


## Install Theme and Font
In the `bundle` folder,

> git clone  https://github.com/jnurmine/Zenburn.git

and in the _vimrc

> colorscheme zenburn

> set number 

To get font compatible to airline

> git clone https://github.com/powerline/fonts.git ~/tmp/powerline_fonts

Then go to the `~/tmp/powerline_fonts`, copy DejaVu_Sans_Mono_for_Powerline font to the Font Floder in Windows, and in _vimrc file:

> if has('gui_running')

> set guifont=Meslo_LG_L_for_Powerline:h12:cANSI

> endif

## Install and use CtrlP
## Install ctags
## Install nerdtree
## Install numbers
## Install tagbar
## Install vim-airline
## Install vim-sensible
## Install YouCompleteMe
## Install vim-colors-solarized

# `vi` usage and shortcuts

## basic commands
`i` to enter the `insert` mode

`a` to append

`c` for change

`d` for delete

`p` for put, or paste

`y` for yank, 

`ESC` to back to the `command` mode

`ZZ` capitalized ZZ to save and quit edits

`:w` to save (write) your file but not quit

`:q` to quit if yyou haven't made any edits

`:wq` to both save and quit, which is equivalent to `ZZ`

`:e!` to returns you to the last saved version of the file, to start over

`:q!` to wipe out the edits and just quit `vi`

`:w!` to overwrite the existing file

## Movements
`h` go to left with one space

`j` go down with one space

`k` go up with one space

`l` go righe with one space

you can use numbers to move multiple times like

`4l` to move right, 4 spaces

`0` move to beginning of the line

`$` move to end of the line ($ just to escape from dollar)

`w` moves the cursor forward one word at a time, counting symbols and punctuation as equivalent to words

`W` captital W will move the cursor forward one word a time without counting symbols and punctuation

`b` move backward by word 

`B` move back by word without counting punctuation

you can also use numbers to move multiple words using `2b`

`G` the `Go to` command, where `G` go to the end of the file, `1G` goes to the first line of the file, and `43G` goes to the 43 line of the file

## Editing
Text object: http://blog.carbonfive.com/2011/10/17/vim-text-objects-the-definitive-guide/

`A` insert from the end of the line

`ciw` replace the current word  and insert

`o` insert from new line.

## Settings
`:set wm=10` can set a `wrapmargin` to 10 characters

`:set nu` will display line numbers

