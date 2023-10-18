how to access connected mobile data
[stackoverflow](https://askubuntu.com/questions/342319/where-are-mtp-mounted-devices-located-in-the-filesystem)


[arch wiki](https://wiki.archlinux.org/title/Vifm)
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
##### as ueberzerg is not working we need to use uerberzergpp
- install by the following instructions [download site for ubuntu](https://software.opensuse.org/download.html?project=home%3Ajustkidding&package=ueberzugpp), following lines are for ubuntu 22.04
```sh
echo 'deb http://download.opensuse.org/repositories/home:/justkidding/xUbuntu_22.04/ /' | sudo tee /etc/apt/sources.list.d/home:justkidding.list
curl -fsSL https://download.opensuse.org/repositories/home:justkidding/xUbuntu_22.04/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/home_justkidding.gpg > /dev/null
sudo apt update
sudo apt install ueberzugpp
```
- copy the scripts vifmrun and vifmimg found in [uebererg++ repo](https://github.com/jstkdng/ueberzugpp)to $PATH directory
- then add the following to vifmrc file, put them in image and pdf section
```txt
    fileviewer *.pdf
        \ vifmimg pdf %px %py %pw %ph %c
        \ %pc
        \ vifmimg clear

    fileviewer <image/*>
        \ vifmimg draw %px %py %pw %ph %c
        \ %pc
        \ vifmimg clear
```
- run vifmrun script 