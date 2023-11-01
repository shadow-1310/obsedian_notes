tags : #linux

set wallpaper
```bash
gsettings set org.gnome.desktop.background picture-uri-dark file:///home/serrano/Pictures/y.jpg
```

check file usage
- https://www.howtogeek.com/409611/how-to-view-free-disk-space-and-disk-usage-from-the-linux-terminal/
### using nvidia
- https://support.system76.com/articles/graphics-switch-ubuntu/

## Packages
- [[Gnome]]
- [[conda]]
- [[Mesa]]
- [[nvim]]
- [[ffmpeg]]
- [[fzf]]
- evince - Document Viewer
- [[apt]]
- [[termdown]]
- [[vifm]]
- [[alacritty]]
- [[tiling window manager]]
- [[qutebrowser]]
- [[firefox]]
- [[imageMagick]]
- [[ncspot]]
- [[mutt]]
- [[MySQL]]
- [[newsboat]]
- [[NewsFlash]]
- [[flatpack]]
## Add and Remove startup programme
### helpful links
- [see all programmes](https://www.maketecheasier.com/manage-startup-applications-ubuntu/)
- [see specific programme](https://www.makeuseof.com/manage-startup-applications-on-ubuntu/#:~:text=To%20add%20a%20new%20program,the%20Add%20Startup%20Program%20window.&text=Alternatively%2C%20you%20can%20click%20Browse,the%20program%3B%20although%20it's%20optional.)
### commands
- see list of startup programmes
```shell
systemd-analyze blame
```
- see if specific programme is on startup
```sh
systemctl list-unit-files | grep <program-name>
```
- disable the programme
```sh
sudo systemctl disable <program-name>
```

## Cool terminal apps
- hollywood style hacking [here](https://www.tecmint.com/fake-hollywood-hacker-terminal/)

```shell
$ sudo apt-add-repository ppa:hollywood/ppa
$ sudo apt-get update
$ sudo apt-get install byobu hollywood
```