# Install Babun
Go to [Babun](http://babun.github.io/), download, unzip and install Babun use cmd, e.g. 

> install.bat /t "D:\Babun"

Wait until the installation finishes, it will bring up a `zsh` with `babun` theme.

# Change theme
Here I want to change the theme from default one to `agnoster` using the already included `oh-my-zsh'

## Install Monaco Powerline font
Go to [Monaco Powerline](https://gist.github.com/kevinis/c788f85a654b2d7581d8), download the font file `Monaco%20for%20Powerline.ttf` by clicking on the `view raw` link, put it into the Windows Font folder, let the installation finish.

## Change .zshrc
Start a fresh babun shell and type

> vim /home/`username`/.zshrc

In top of the `.zshrc` file, add

> DEFAULT_USER=xli

Change the theme from `babun` to `agnoster`. Save and exit `vim`. More can find in [YangHu's .zshrc](https://github.com/yanghu/dotfiles/blob/master/.zshrc)

## Change .minttyrc
Same as `cgywin`, `babun` is also use the `mintty` as the shell emulator. So to change the color theme and font need to be set in the `.minttyrc`. The color theme selected here is the [mintty-colors-solarized](https://github.com/mavnn/mintty-colors-solarized) .

The `.minttyrc` file will be

> Font=Monaco for Powerline

> FontHeight=12

> ForegroundColour=131, 148, 150

> BackgroundColour=  0,  43,  54

> CursorColour=    220,  50,  47

> Black=             7,  54,  66

> BoldBlack=         0,  43,  54

> Red=             220,  50,  47

> BoldRed=         203,  75,  22

> Green=           133, 153,   0

> BoldGreen=        88, 110, 117

> Yellow=          181, 137,   0

> BoldYellow=      101, 123, 131

> Blue=             38, 139, 210

> BoldBlue=        131, 148, 150

> Magenta=         211,  54, 130

> BoldMagenta=     108, 113, 196

> Cyan=             42, 161, 152

> BoldCyan=        147, 161, 161

> White=           238, 232, 213

> BoldWhite=       253, 246, 227


# Setup `vim`

## Install `pathogen.vim` 

> mkdir -p ~/.vim/autoload ~/.vim/bundle

> curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim

