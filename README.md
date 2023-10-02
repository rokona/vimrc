![VIM](https://dnp4pehkvoo6n.cloudfront.net/43c5af597bd5c1a64eb1829f011c208f/as/Ultimate%20Vimrc.svg)

# The Ultimate vimrc

There are two versions:

* **The Basic**: If you want something small just copy [basic.vim](https://github.com/rokona/vimrc/blob/master/vimrcs/basic.vim) into your ~/.vimrc and you will have a good basic setup
* **The Awesome**: Includes a ton of useful plugins, color schemes, and configurations

I would, of course, recommend using the awesome version.


## How to install the Awesome version?
### Install for your own user only
The awesome version includes a lot of great plugins, configurations and color schemes that make Vim a lot better. To install it simply do following from your terminal:

	git clone --depth=1 https://github.com/rokona/vimrc.git ~/.vim_runtime
	sh ~/.vim_runtime/install_awesome_vimrc.sh
	
### Install for multiple users
To install for multiple users, the repository needs to be cloned to a location accessible for all the intended users.

	git clone --depth=1 https://github.com/rokona/vimrc.git /opt/vim_runtime
	sh /opt/vim_runtime/install_awesome_parameterized.sh /opt/vim_runtime user0 user1 user2
	# to install for all users with home directories, note that root will not be included
	sh /opt/vim_runtime/install_awesome_parameterized.sh /opt/vim_runtime --all
	
Naturally, `/opt/vim_runtime` can be any directory, as long as all the users specified have read access.

## Fonts

I recommend using [IBM Plex Mono font](https://github.com/IBM/plex) (it's an open-source and awesome font that can make your code look beautiful). The Awesome vimrc is already setup to try to use it.

Some other fonts that Awesome will try to use:

* [Hack](http://sourcefoundry.org/hack/)
* [Source Code Pro](https://adobe-fonts.github.io/source-code-pro/)

## How to install the Basic version?

The basic version is just one file and no plugins. Just copy [basic.vim](https://github.com/rokona/vimrc/blob/master/vimrcs/basic.vim) and paste it into your vimrc.

The basic version is useful to install on remote servers where you don't need many plugins, and you don't do many edits.

	git clone --depth=1 https://github.com/rokona/vimrc.git ~/.vim_runtime
	sh ~/.vim_runtime/install_basic_vimrc.sh


## How to update to latest version?

Just do a git rebase!


    cd ~/.vim_runtime
    git reset --hard
    git clean -d --force
    git pull --rebase
    python update_plugins.py  # use python3 if python is unavailable


## How to uninstall
Just do following:
* Remove `~/.vim_runtime`
* Remove any lines that reference `.vim_runtime` in your `~/.vimrc`

