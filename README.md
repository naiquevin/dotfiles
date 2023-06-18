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
