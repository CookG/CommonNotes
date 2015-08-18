#Install iTerm2

[Download](http://www.iterm2.com/downloads.html) and Install iTerm2/

#Change to zsh

* Use command to change shell to zsh

> chsh -s /bin/zsh

* Find out which shell is using

> echo $SHELL

#Install [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)

* Run the following 

> curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh

if met error "Agreeing to the Xcode/iOS license requires admin privileges, please re-run as root via sudo", it may mean there is a new version of Xcode was downloaded and need open up Xcode and accept new user agreement.

* Edit `~/.zshrc` and set `ZSH_THEME="agnoster"`

* Set defult user `DEFAULT_USER=huey`

#Change theme
[Solorized Dark Theme](https://raw.githubusercontent.com/altercation/solarized/master/iterm2-colors-solarized/Solarized%20Dark.itermcolors)

Apply it in iTerm through iTerm -> preferences -> profiles -> colors -> load presets. Don't forget to select it...

#Install supported font
[Monaco for Powerline](https://gist.github.com/kevinis/c788f85a654b2d7581d8)

Open the downloaded font and press "Install Font".

Set this font in iTerm2 (iTerm -> preferences -> profiles -> text).

Regular Font -> "Change Font"

Non-ASCII Font -> "Change Font"

Restart iTerm for all changes to take effect.

#To install macvim
* install homebrew from [install homebrew](http://brew.sh)
* Run `export PATH=/usr/local/bin:$PATH`
* Run `brew update && brew upgrade`
* Run `brew install vim && brew install macvim`
* Run `brew linkapps macvim`

#To update macvim
* Run `brew update && brew upgrade`
