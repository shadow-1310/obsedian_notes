## integrate fzf
- open the .config/vifm/vifmrc file
- put the following lines
	- https://wiki.vifm.info/index.php/How_to_integrate_fzf_for_fuzzy_finding
	```sh
	command! FZFfind : set noquickview
                \| let $FZF_PICK = term('find | fzf --height 10 2>/dev/tty')
                \| if $FZF_PICK != ''
                \|     execute 'goto' fnameescape($FZF_PICK)
                \| endif
                
	nnoremap <c-f> :FZFfind<cr>
	```

## use image previews with uberzug
- https://www.youtube.com/watch?v=qgxsduCO1pE
- https://gitlab.com/dwt1/dotfiles/-/tree/master/.config/vifm/scripts