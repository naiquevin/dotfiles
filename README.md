dotfiles
========

All my dotfiles, managed using
[stow](https://www.gnu.org/software/stow/).

Usage
-----

Clone this repo, and then run,

``` bash
    $ stow -vv --dotfiles -d /path/to/dotfiles -t ~ tmux
```

In the above command, the final argument `tmux` is a "package" and it
corresponds to the directory "tmux" inside this project root. The
above command causes the dotfiles present inside the package dir
`tmux` to be stowed to the target directory `~`.

Known Issues
------------

The `--dotfiles` option doesn't work well with subdirectories with the
dot prefix. For example, for `.emacs.d` directory inside the root, the
subdirectory under `emacs` package can't be named `dot-emacs.d`. So
it's named `.emacs.d` which works. Apparently, this [bug has been
fixed](https://github.com/aspiers/stow/issues/33) long ago but a new
version of stow hasn't been released since.
