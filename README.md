# Inspiration Dotfiles :fire:
by: (Cesar Gomez)

compatibility: Mac OS


### Requirements
The installation step requires the [XCode Command Line
Tools](https://developer.apple.com/downloads) and may overwrite existing
dotfiles in your HOME and `.dotfiles, .vim` directories.

lastest zsh from brew
```bash
brew install zsh
```
or
```bash
brew upgrade zsh
```

I recommend to use Iterm2 nightly build
https://www.iterm2.com/nightly/latest

## How to install

Run
```bash
curl -L raw.github.com/cesargomez89/inspiration-dotfiles/master/bin/dotfiles | bash
```
the first time openning neovim you have to use:
```vim
:PlugInstall
```
to install all the plugins, then reopen nvim.

If you wish to fork this project and maintain your own dotfiles, you must
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

### Zsh

* [Prezto :heart:](https://github.com/sorin-ionescu/prezto)

### Tmux

* [Tmux Plugin Mangager :package:](https://github.com/tmux-plugins/tpm)
* [Tmuxinator :goberserk:](https://github.com/tmuxinator/tmuxinator)
* [Tmux Resurrect :skull:](https://github.com/tmux-plugins/tmux-resurrect)
* [Shpotify :green_apple:](https://github.com/hnarayanan/shpotify)

### Neovim

* [Async Plugins installer](https://github.com/junegunn/vim-plug)
* [fuzzy finder (ctrl+p)](https://github.com/junegunn/fzf)
* [atags(ctags aync gen)](https://github.com/fntlnz/atags.vim)
* [async autocomplete](https://github.com/Shougo/deoplete.nvim)
* [Neomake (detect ruby syntax)](https://github.com/neomake/neomake)
* nerdtree
* tmux navigation and navbar
* multicursor

### Automatic software installation

Homebrew useful tools:

* GNU core utilities
* bash (latest version)
* [git](http://git-scm.com/)
* [the silver searcher](https://github.com/ggreer/the_silver_searcher)
* [ctags](https://github.com/universal-ctags/homebrew-universal-ctags)
* [zsh](https://sourceforge.net/projects/zsh/files/)
* [bash-completion](http://bash-completion.alioth.debian.org/)
* [macvim](http://code.google.com/p/macvim/)
* [neovim](https://neovim.io/)
* [rsync](https://rsync.samba.org/) (latest version, rather than the out-dated OS X installation)
* [tree](http://mama.indstate.edu/users/ice/tree/)
* [wget](http://www.gnu.org/software/wget/)
* [ssh-copy-id]
* [tmux](http://tmux.sourceforge.net/)
* [reattach-to-user-namespace](https://github.com/ChrisJohnsen/tmux-MacOSX-pasteboard)
* [tmate](http://tmate.io)
* [Shpotify](https://github.com/hnarayanan/shpotify)

### Shortcuts & Commands

[My own shortcuts and commands](/shell/shell_aliases)

[Zprezto](https://github.com/sorin-ionescu/prezto/tree/master/modules)

Prezto has implemented many shortcuts used by the community. Here are the ones I'm using:
```
  autosuggestions
  environment
  terminal
  editor
  history
  history-substring-search
  homebrew
  directory
  node
  osx
  rails
  rsync
  ruby
  syntax-highlighting
  spectrum
  terminal
  utility
  completion
  git
  tmux
  prompt
```

### Custom OS X defaults

Custom OS X settings can be applied during the `dotfiles` process. They can
also be applied independently by running the following command:

```bash
$ osxdefaults
```

### Custom shell prompt

Iterm theme:
[Monokai Soda](https://github.com/mbadolato/iTerm2-Color-Schemes#monokai-soda)

Font:
[Inconsolata Powerline Nerd Font](/files/inconsolata_nerd_font_complete.otf)
Remember to set the font in iterm2 profile

Neovim Dotfiles Only: https://github.com/cesargomez89/neovim-dotfiles

Screenshot:

![Alt text](/files/screenshot.png)

### Local/private Bash configuration

N.B. Because the `git/gitconfig` file is copied to `~/.gitconfig`, any private
git configuration specified in `~/.bash_profile.local` will not be committed to
your dotfiles repository.
