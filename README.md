# Dotfiles (Cesar Gomez)

My OS X dotfiles.


## How to install

The installation step requires the [XCode Command Line
Tools](https://developer.apple.com/downloads) and may overwrite existing
dotfiles in your HOME and `.dotfiles, .vim` directories.

```bash
$ bash -c "$(curl -fsSL raw.github.com/cesargomez89/inspiration-dotfiles/master/bin/dotfiles)"
```

N.B. If you wish to fork this project and maintain your own dotfiles, you must
substitute my username for your own in the above command and the 2 variables
found at the top of the `bin/dotfiles` script.

## How to update

You should run the update when:

* You make a change to `~/.dotfiles/git/gitconfig` (the only file that is
  copied rather than symlinked).
* You want to pull changes from the remote repository.
* You want to update Homebrew formulae and Node packages.

Run the dotfiles command:

```bash
$ dotfiles
```

## Features

### Automatic software installation

Homebrew formulae:

* GNU core utilities
* [git](http://git-scm.com/)
* [ack](http://betterthangrep.com/)
* the silver searcher
* bash (latest version)
* [bash-completion](http://bash-completion.alioth.debian.org/)
* [macvim](http://code.google.com/p/macvim/)
* [phantomjs](http://phantomjs.org/)
* [rsync](https://rsync.samba.org/) (latest version, rather than the out-dated OS X installation)
* [tree](http://mama.indstate.edu/users/ice/tree/)
* [wget](http://www.gnu.org/software/wget/)
* [ssh-copy-id]
* [tmux](http://tmux.sourceforge.net/)
* [reattach-to-user-namespace](https://github.com/ChrisJohnsen/tmux-MacOSX-pasteboard)
* [tmate](http://tmate.io)
* nvm
* v8
* chromedriver
* qt

### Custom OS X defaults

Custom OS X settings can be applied during the `dotfiles` process. They can
also be applied independently by running the following command:

```bash
$ osxdefaults
```

### Custom bash prompt

Iterm theme [Monokai Soda](https://github.com/mbadolato/iTerm2-Color-Schemes#monokai-soda)

Screenshot:

![Alt text](/screenshots/inspiration-screenshot.png)

### Local/private Bash configuration

N.B. Because the `git/gitconfig` file is copied to `~/.gitconfig`, any private
git configuration specified in `~/.bash_profile.local` will not be committed to
your dotfiles repository.
