tags: #tool/finder

tutorial - [The Amazing Interactive Command Line Fuzzy Finder (fzf) - YouTube](https://www.youtube.com/watch?v=Ab6cWN9ZrXo)
## exclude certain directories
- install ag or rg
- add the following lines to .bashrc
	- https://github.com/BurntSushi/ripgrep/discussions/2128
	- 
	```sh
	#determines search program for fzf
	if type ag &> /dev/null; then
		export FZF_DEFAULT_COMMAND='ag -p ~/.gitignore -g ""'
	fi
	#refer rg over ag
	if type rg &> /dev/null; then
		export FZF_DEFAULT_COMMAND='rg --files --hidden --no-follow -g "!{**/venv/*, **/.git/*}"'
	fi
	```