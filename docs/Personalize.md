# Personalization

In addition to extending SAP Business Application through installation of [VS Code Extensions](Explore_and_Install_VS_Code_Extensions_d83a580.md), [Generators](Explore_and_Install_Generators_7865b5e.md) or [custom SAP Business Application Extensions](Create_and_Deploy_an_SAP_Business_Application_Studio_Extension_2064b4e.md) you can use a well-known personalization technic which is called `dotfiles`.

## tl;dr

There is a wonderful [HandsOnDev recording](https://www.youtube.com/watch?v=YrrxWdIjqEE) which shed a bit of light into this topic.

## What are these so called `dotfiles`?

Dotfiles are plain text configuration files on Unix-y systems for things like our shell, `~/.bashrc`, our editor in `~/.theia/settings.json`, and many others. They are called `dotfiles` as they typically are named with a leading `.` making them hidden files on your system, although this is not a strict requirement.

Since these files are all plain text, we can gather them together in a Git repository and use that to track the changes you make over time.

## Getting Started

It’s pretty simple to get started. You need to organize your dotfiles in some directory. You could do this practically anywhere, like a USB drive or something. Since version control is great, a hosted Git repository like GitHub is a great option to store your `dotfiles`.

## Structure

Below is the structure of a typical `dotfiles` repository. It’s also what we’ll use in our walk-through below.

```
.
├── shell
│ ├── bash_aliases
│ └── bashrc
│ └── profile
├── git
│ └── gitconfig
├── npm
│ └── npmrc
├── theia
│ ├── keymaps.json
│ └── settings.json
├── install.sh
└── README.md
```

## The `dotfiles`

We’ll be taking a look at the following examples:

- install.sh
- .profile
- .bash_aliases
- gitconfig
- settings.json

### `install.sh`

The `install.sh` is your bootstrap script which does all the hard work. It copys all mentioned files from your cloned `dotfiles` into the `HOME` directory.

```shell
#!/usr/bin/env bash
DOTFILES_ROOT=$(pwd -P)

set -e
echo ''

info () {
  printf "\r  $1\n"
}

success () {
  printf "\r\033[2K  [ \033[00;32mOK\033[0m ] $1\n"
}

copy() {
  # Force copy
  cp $1 $2
  success "copied $1 to $2"
}

info "📦 copying dot files"
copy "${DOTFILES_ROOT}/shell/inithomedir" "${HOME}/.inithomedir"
copy "${DOTFILES_ROOT}/shell/profile" "${HOME}/.profile"
copy "${DOTFILES_ROOT}/shell/bash_aliases" "${HOME}/.bash_aliases"
copy "${DOTFILES_ROOT}/shell/bashrc" "${HOME}/.bashrc"
copy "${DOTFILES_ROOT}/git/git-completion.bash" "${HOME}/.git-completion.bash"
copy "${DOTFILES_ROOT}/git/gitconfig" "${HOME}/.gitconfig"
copy "${DOTFILES_ROOT}/npm/npmrc" "${HOME}/.npmrc"
success "copying dot files successful..."

echo ''
info '🧢🧢🧢 Everything set up, maybe reload your BAS! 🧢🧢🧢'
```

### `profile`

In a Bash shell, this file in your home directory is loaded first. What to put in the `.profile` and other dotfiles is truly worth a book alone, but we’re going to give it a quick shot here anyway. It is recommended to use a small `.profile` that links to several other files that have a dedicated purpose, i.e. one file for the aliases, one for the functions, etc. Here’s an example of how you can include (or actually “source”) all files in a folder:

```shell
# if running bash
if [ -n "$BASH_VERSION" ]; then
    # include .bashrc if it exists
    if [ -f "$HOME/.bashrc" ]; then
	. "$HOME/.bashrc"
    fi
fi
```

### `bash_aliases`

Aliases allow you to define shortcuts for commands, to add default arguments, and/or to abbreviate longer one-liners. Here are some examples:

```shell
alias ls='ls --color=auto -ACF --group-directories-first'
alias lsa='ls -la --group-directories-first'
alias ll='ls --color=auto -alF --group-directories-first'

alias cd..='cd ..'
alias ..='cd ..'
alias ...='cd ../..'
alias ....='cd ../../..'

alias glog='git log --oneline --all --graph --decorate --color $*'
alias gs='git status -s'
```

### `bashrc`

You put commands here to set up the shell for use in your particular environment, or to customize things to your preferences. A common thing to put in `.bashrc` is a custom prompt. In the example below the last line will change our default SAP Business Application Studio terminal prompt to include some colors and the actual Git branch (if the current directory is a git repository).

```shell
export TERM=xterm-256color

txtgrn='\[\e[0;32m\]' # Green
bldcyn='\[\e[1;36m\]' # Cyan
bldred='\[\e[1;31m\]' # Red
bldgrn='\[\e[1;32m\]' # Green
txtrst='\[\e[0m\]'    # Text Reset

gitBranch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}

export PS1="${txtgrn}➜ ${bldcyn}\w ${bldred}\$(gitBranch)\n${bldgrn}\$${txtrst} "
```

### `gitconfig`

The `gitconfig` file configures your settings for Git, e.g. your E-Mail and name.

```shell
[user]
	email = john.doe@sap.com
	name = John Doe
```

### `settings.json`

The `settings.json` file configures the default behavior for SAP Business Application Studio. In the following example we have some settings for the editor itself and the integrated terminal.

```json
{
  "editor.fontFamily": "Fira Code, Consolas, 'Courier New', monospace",
  "editor.fontLigatures": true,
  "editor.fontSize": 15,
  "editor.cursorBlinking": "smooth",
  "editor.cursorSmoothCaretAnimation": true,
  "editor.cursorStyle": "line",
  "editor.autoSaveDelay": 30000,
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "editor.renderIndentGuides": true,
  "editor.smoothScrolling": true,
  "editor.hover.enabled": false,
  "workbench.editor.highlightModifiedTabs": true,
  "terminal.integrated.fontWeightBold": "normal",
  "terminal.integrated.fontFamily": "Fira Code",
  "terminal.integrated.cursorBlinking": true,
  "terminal.integrated.cursorStyle": "underline"
}
```
