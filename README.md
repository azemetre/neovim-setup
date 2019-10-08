# my neovim setup

## prerequisites
### [homebrew](https://brew.sh/)
If you don't have homebrew installed for macOS, please install it with the following command:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

This setup relies on [FZF](https://github.com/junegunn/fzf), [Python](https://www.python.org/), [Node.js](https://nodejs.org/en/), and obviously [neovim](https://neovim.io/).

Use the following commands to install these dependencies:
```
brew install neovim fzf python node
```

**Please Note:** if you use [nvm](https://github.com/nvm-sh/nvm) and plan on using [TypeScript](https://github.com/microsoft/TypeScript). It is recommended you have a global node installed on your machine to use [coc-tsserver](https://github.com/neoclide/coc-tsserver) between node environments.

If you don't use [nvm](https://github.com/nvm-sh/nvm) you do not need to install node with homebrew.

### python
To verify you have python3 installed with the following commands:
`python3 --version` or `python --version`

After confirming you have the python3 installed, please install the following pip dependencies:
```
pip3 install pynvim neovim
```

### node
Verify you have Node.js installed with the following command:
`node --version`

If you're using [nvm](https://github.com/nvm-sh/nvm), it is highly recommended to have a global [Node.js](https://nodejs.org/en/) on your machine. In order to use [coc-tsserver](https://github.com/neoclide/coc-tsserver) you need to install the following node dependencies:

* [yarn](https://yarnpkg.com/en/)
* [neovim](https://github.com/neovim/node-client)
* [TypeScript](https://github.com/microsoft/TypeScript)

Prior to install global dependencies, please be sure to deactivate nvm with the following command:
```
nvm deactivate
```

Then install the dependencies globally with the following:
```
npm i -g yarn neovim typescript
```


### installing vim-plug
[Vim-Plug](https://github.com/junegunn/vim-plug) is required.

Follow [installation instructions](https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim) prior to pulling `.vimrc`.

After installing [Vim-Plug](https://github.com/junegunn/vim-plug) and copying `.vimrc` into your home directory. Open the file with the following command in your command line terminal:
```
nvim .vimrc
```

While in your `.vimrc` file type in the following to install the vim plugins:
```
:PlugInstall
```

## requisites
### [coc.nvm](https://github.com/neoclide/coc.nvim)

Copy the `.config/` directory into your home path. The only setting that may change is the path of your global npm. To verify what your path is deactivate nvm with `nvm deactivate` and use the following command to find your npm path:
```
which npm
```

The output of the above command should go into the tsserver.npm property in your `coc-settings.json`, a partial example listed below:
```
"tsserver.npm": "/usr/local/bin/npm"
```

## end game
Congrats! You've installed my [neovim](https://neovim.io/) + [configuration](https://github.com/azemetre/neovim-setup) successfully on your machine.


### to-dos
- ~~commit my .vimrc~~
- describe hot keys
- state why coc.nvim is used for LSP and how to configure it properly
- justify why the settings and plugins were choosen
- show screenshots of color palattes
- write synopsis on why I use vim
- group plugins by environment types (python, typescript + react + css, go support, etc)
