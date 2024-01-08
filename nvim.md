tags : 
## configs
---
- config by Neural Nine [here](https://github.com/NeuralNine/config-files/blob/master/init.vim)

## Plugins
---
### coc.nvm - autocompletion 
[github-repo](https://github.com/neoclide/coc.nvim)
#### setup
1. install nodejs
 ```sh
	sudo apt install nodejs
```
2. install npm
```sh
sudo apt install npm
```
 
3. Put Plugin call in .config file (init.vim)
- first open init.vim
```sh
nvim ~/.config/nvim/init.vim
```
- put the text inside init.vim
```txt
call plug#begin()
Plug 'https://github.com/neoclide/coc.nvim'  " Auto Completion
call plug#end()
```
4. install the plugin in nvim terminal
```sh
:PlugInstall
```
5. Now go to plugin installation directory. which can be
- in user/share like below
```sh
cd ~/.local/share/nvim/plugged/coc.nvim
```
- or in .config location
```sh
cd ~/.config/nvim/plugged/coc.nvim
```
6. install yarn in that directory
```sh
	yarn install
```
- if there is a problem with yarn install like below - (to upgrade nodejs). 
	- ![[Pasted image 20230722225636.png]]
	- run the following commands to upgrade nodejs
		```sh
		sudo npm cache clean -f
		sudo npm install -g n
		sudo n stable
		```
7. Build yarn in that directory
```sh
yarn build
```
8. install module for python coc-python by running the following in nvim terminal
```txt
:CocInstall coc-python
```
or for scala
```
:CocInstall coc-metals
```

### select interpreter of virtual env

^148240

- <code>:CocCommand</code> then select <code>python.setInterpreter</code>
### problems
- when selecting a new python interpreter, it shows error 
<code>cannot perform a user install, site packages are not visible in this virtual environment</code>
- then manually install pylint in the environment first
 ```python
pip install -U pylint
```
### fzf
tutorial - [Vim Plugin Highlight: fzf.vim! Fuzzy File Finding Fun! - YouTube](https://www.youtube.com/watch?v=DpURGnb4Fyk)

#### make transparent
```.init
highlight Normal ctermbg=none
highlight NonText ctermbg=none
```
## keyboard shortcuts
---
- indent lines [stackoverflow](https://stackoverflow.com/questions/235839/indent-multiple-lines-quickly-in-vi)
- leader key
	- https://stackoverflow.com/questions/1764263/what-is-the-leader-in-a-vimrc-file
- enclose in parenthesis [Enclosing in parentheses with Vim - Stack Overflow](https://stackoverflow.com/questions/8070892/enclosing-in-parentheses-with-vim) ^63e2b2
- opening vertical window, [How to open files in vertically/horizontal split windows in Vim from the command line - Super User](https://superuser.com/questions/486532/how-to-open-files-in-vertically-horizontal-split-windows-in-vim-from-the-command) ^64fa21
- find and replace
	- https://stackoverflow.com/questions/25684559/what-is-the-difference-between-g-and-s-commands-in-vim
	- https://stackoverflow.com/questions/7598133/how-to-search-and-replace-globally-starting-from-the-cursor-position-and-wrappi
	```sh
	:,$s/before/after/gc
	```
	- here g means globally, i.e every occurrence in a line
	- c is there if you want to ask for confirmation prompt

### good use cases
- [automatically get list of files in a dir](https://www.youtube.com/watch?v=hraHAZ1-RaM
- [resize splits](https://vi.stackexchange.com/questions/514/how-do-i-change-the-current-splits-width-and-height)
- [delete marks](https://stackoverflow.com/questions/11450817/vim-how-do-i-clear-all-marks)
- [surround character](https://vi.stackexchange.com/questions/22930/how-to-use-surround-vim-to-quote-a-single-character)

## Setting airline theme with power fonts
- [powerline fonts repo](https://github.com/powerline/fonts)
- https://github.com/vim-airline/vim-airline/wiki/Screenshots
- https://ianchanning.wordpress.com/2018/06/18/vim-airline-powerline-fonts-on-fedora-ubuntu-and-windows/
- https://vi.stackexchange.com/questions/3359/how-do-i-fix-the-status-bar-symbols-in-the-airline-plugin


## LSP
- [LSP server list](https://github.com/williamboman/mason-lspconfig.nvim#available-lsp-servers)
#### how to setup a new lsp
- download the lsp binary from its source, maybe npm, or other package manager
- then make a setting file in lua/user/lsp/setting
- include the server name in mason.lua