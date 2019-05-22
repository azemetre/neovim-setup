# my neovim setup

### [homebrew](https://brew.sh/) prerequisites
This setup relies on [FZF](https://github.com/junegunn/fzf), [Python](https://www.python.org/), and obviously [neovim](https://neovim.io/).

Use the following commands to install these dependencies:
```
brew install neovim fzf python
```

### python dependencies
To verify you have python3 installed with the following commands:
`python3 --version` or `python --version`

After confirming you have the python3 installed, please install the following pip dependencies:
```
pip3 install pynvim neovim
```

### installing vim-plug
[Vim-Plug](https://github.com/junegunn/vim-plug) is required.

Follow [installation instructions](https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim) prior to pulling `.vimrc`.

After installing [Vim-Plug](https://github.com/junegunn/vim-plug) and copying `.vimrc` into your root directory. Open the file with the following command in your command line terminal:
```
nvim .vimrc
```

While in your `.vimrc` file type in the following to install the vim plugins:
```
:PlugInstall
```

Congrats! You've installed my `.vimrc` environment successfully on your machine.
