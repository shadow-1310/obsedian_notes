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


### fzf
tutorial - [Vim Plugin Highlight: fzf.vim! Fuzzy File Finding Fun! - YouTube](https://www.youtube.com/watch?v=DpURGnb4Fyk)


## keyboard shortcuts
---
- indent lines [stackoverflow](https://stackoverflow.com/questions/235839/indent-multiple-lines-quickly-in-vi)