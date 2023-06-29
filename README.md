# Inspiration Dotfiles :fire:
by: (Cesar Gomez)

compatibility: Mac OS, Linux


### Requirements
- MacOS Only

The installation step requires the [XCode Command Line
Tools](https://developer.apple.com/downloads)

I recommend to use iTerm2 nightly build
https://www.iterm2.com/nightly/latest

- General
  - git
  - zsh
  - tmux
  - neovim


Ensure you have valid public key linked to your github account.

Set zsh as default shell
`chsh -s $(which zsh)`
    
This script may overwrite existing dotfiles in your HOME and `.dotfiles, .vim` directories.

## How to install

Run
```bash
curl -L raw.github.com/cesargomez89/inspiration-dotfiles/master/bin/dotfiles | bash
```

### After Install

The first time openning neovim you have to use: `:PlugInstall` to install all the plugins,
then reopen nvim.

In order to get the font icons working you have to install the respective nerd font. The current font is [Insconsolata Nerd Font](https://github.com/ryanoasis/nerd-fonts).
After install it, just set the font in your current terminal profile.

The custom tmux binding is `C-a` (Ctrl + a).
To get all the tmux plugins working run:
`C-a I` install all the plugins.
`C-a U` and type `all` to update all the plugins.

For NeoVim Coc extensions run:

nvim +'CocInstall -sync coc-git coc-fzf-preview coc-solargraph coc-highlight' +qall

Further information: [TPM](https://github.com/tmux-plugins/tpm)

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
  * 'tmux-plugins/tpm'
  * 'tmux-plugins/tmux-sensible'
  * 'tmux-plugins/tmux-yank'
  * 'tmux-plugins/tmux-resurrect'
  * 'tmux-plugins/tmux-continuum'
  * 'tmux-plugins/tmux-sessionist'
  * 'tmux-plugins/tmux-pain-control'
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
* [zsh](https://sourceforge.net/projects/zsh/files/)
* [neovim](https://neovim.io/)
* [wget](http://www.gnu.org/software/wget/)
* [tmux](http://tmux.sourceforge.net/)
* [Shpotify](https://github.com/hnarayanan/shpotify) (Mac OS)
* [ctags](https://github.com/universal-ctags/homebrew-universal-ctags) (Mac OS)
* [rsync](https://rsync.samba.org/) (latest version, rather than the out-dated OS X installation)
* [reattach-to-user-namespace](https://github.com/ChrisJohnsen/tmux-MacOSX-pasteboard) (Mac OS)

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
[Monokai Soda Raw](https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/Monokai%20Soda.itermcolors)

Font:
[Inconsolata Powerline Nerd Font](/files/inconsolata_nerd_font_complete.otf)
Remember to set the font in iterm2 profile

Neovim Dotfiles Only: https://github.com/cesargomez89/neovim-dotfiles

Screenshot:

![Alt text](/files/screenshot.png)

### Forking

If you wish to fork this project and maintain your own dotfiles, you must
substitute my username for your own in the above command and the 2 variables
found at the top of the `bin/dotfiles` script.

```bash
~/.dotfiles >>> git grep cesargomez

.gitmodules:3:  url = git@github.com:cesargomez89/themes.git
README.md:25:curl -L raw.github.com/cesargomez89/inspiration-dotfiles/master/bin/dotfiles | bash
README.md:148:Neovim Dotfiles Only: https://github.com/cesargomez89/neovim-dotfiles
bin/dotfiles:2:DOTFILES_TARBALL_PATH="https://github.com/cesargomez89/inspiration-dotfiles/tarball/master"
bin/dotfiles:3:DOTFILES_GIT_REMOTE="git@github.com:cesargomez89/inspiration-dotfiles.git"
git/gitconfig:16:    # Use: `git browse https://github.com/cesargomez89/inspiration-dotfiles <commit-ish>`
lib/help:6:OS X dotfiles - Cesar Gomez - http://cesargomez89.github.io/
lib/help:16:Documentation can be found at https://github.com/cesargomez89/inspiration-dotfiles/
lib/list:7:OS X dotfiles - Cesar Gomez - http://cesargomez.github.io/
```
