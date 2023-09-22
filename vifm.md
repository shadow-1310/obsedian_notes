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

## Setting airline theme with power fonts
- [powerline fonts repo](https://github.com/powerline/fonts)
- https://github.com/vim-airline/vim-airline/wiki/Screenshots
- https://ianchanning.wordpress.com/2018/06/18/vim-airline-powerline-fonts-on-fedora-ubuntu-and-windows/
- https://vi.stackexchange.com/questions/3359/how-do-i-fix-the-status-bar-symbols-in-the-airline-plugin