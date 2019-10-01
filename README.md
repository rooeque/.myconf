# myconf
dotfiles

### Installation
Pull/Clone this repo into your `$HOME` directory

##### iTerm
In `Preferences -> General`, select: "Load preferences from a custom folder". Choose your `$HOME` directory

### Customization

This repo comes with the alias
`alias config='/usr/bin/git --git-dir=$HOME/.myconf/ --work-tree=$HOME'` so you don't have to declare your working tree each time

`Oh-My-Zsh`, `NerdTree`, and the `zsh-syntax-highlighting` plugin are all in submodules. `oh-my-zsh` tracks a fork on my personal Github, but the others just track their respective base repo. It's highly suggested to fork and track your own `oh-my-zsh` as a submodule (and perhaps the other submodules as well) if you intend on further customizing your preferences. 

Whenever you change any configuration file/directory **NOT** in a submodule, simply run
`config add [YOUR FILE/DIRECTORY HERE]`, and from then on commit and push as usual

If you change a configuration file/directory in a submodule, you'll need to track a fork of it to intake those changes. After you've finished changing the submodule, simply `cd` into the submodule directory and `git push` as usual

To update all submodules from your $HOME directory, run

`git submodule foreach git pull upstream master`

You can then go ahead and run `config add [SUBMODULE HERE]` and commit and push as usual

