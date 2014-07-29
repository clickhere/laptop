Laptop
======

Laptop is a script to set up a Mac OS X laptop for Rails development.

Requirements
------------

### Mac OS X

Install a C compiler:

For Snow Leopard (10.6): use [OS X GCC
Installer](https://github.com/kennethreitz/osx-gcc-installer/).

For Lion (10.7) or Mountain Lion (10.8): use [Command Line Tools for
XCode](https://developer.apple.com/downloads/index.action).

For Mavericks (10.9): installed with the script, no prerequisite.

For Yosemite (10.10): installed with the script, no prerequisite.

Install
-------

### Mac OS X

Read, then run the script:

    bash <(curl -s https://raw.githubusercontent.com/clickhere/laptop/master/mac) | tee ~/laptop.log

Debugging
---------

Your last Laptop run will be saved to `~/laptop.log`. Read through it to see if
you can debug the issue yourself. If not, copy the lines where the script
failed into a [new GitHub
Issue](https://github.com/clickhere/laptop/issues/new) for us. Or, attach the
whole log file as an attachment.

What it sets up
---------------

* Zsh as your shell
* Homebrew for managing operating system libraries
* Rbenv for managing versions of the Ruby programming language
* Ruby Build for installing Rubies
* Ruby stable for writing general-purpose code
* Bundler gem for managing Ruby libraries
* Rails gem for writing web applications
* MySQL database for storing relational data
* Postgres database for storing relational data
* Redis for storing key-value data
* Node.js and NPM, for running apps and installing JavaScript packages
* Vim for text editing from terminal
* Exuberant Ctags for indexing files for vim tab completion
* Tmux for saving project state and switching between projects
* The Silver Searcher for finding things in files
* Hub gem for interacting with the GitHub API
* ImageMagick for cropping and resizing images

It should take less than 20 minutes to install (depends on your machine).

Laptop can be run multiple times on the same machine safely. It will upgrade
already installed packages and install and activate a new version of ruby (if
one is available).

Workspace
---------

A directory called 'code' has been created in your home directory so all your
projects can be saved there. This will be your "workspace".

A `c` shortcut has also been created for your terminal. At the prompt, type
the letter "c" (without quotation marks) then `SPACE` + `TAB` to list your
workspace directories. You can then start to type a workspace directory name
and `TAB` again to complete.

Make your own customizations
----------------------------

Put your customizations in `~/.laptop.local`. For example, your
`~/.laptop.local` might look like this:

    #!/bin/sh

    brew tap caskroom/cask
    brew install brew-cask

    brew cask install dropbox
    brew cask install google-chrome
    brew cask install rdio

You should write your customizations such that they can be run safely more than
once. See the `mac` script for examples.

Contributing
------------

Please see [CONTRIBUTING.md](https://github.com/clickhere/laptop/blob/master/CONTRIBUTING.md).
