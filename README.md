## dotctl

Dotfiles management system. Inspired by rcm.

This tools creates symlinks from your **git managed** dotfiles into your home directory (or the directory of your choice).

### Features

* Files can be ignored.
* Whole directories can be symlinked instead of each file.
* Post up hook.
* Status of the dotfiles.


### Requirements

Only basic unix tools are required:
* awk
* git
* grep
* ln
* sed
* uniq
* wc

### Configuration

This program is configured using environment variables.

```sh
# Your dotfiles location
export DOTCTL_DOTFILES_DIR="$HOME/.dotfiles"
# Were to install your config files
export DOTCTL_DOTFILES_DESTDIR=$HOME
# Files to ignore during install
export DOTCTL_EXCLUDES=".gitignore .gitmodules"
# Directories to symlink (without creating a symlink for each file)
export DOTCTL_SYMLINK_DIRS="vim"
# Verbose output
export DOTCTL_VERBOSE=0
# Disable hooks
export DOTCTL_NO_HOOK=1
```
