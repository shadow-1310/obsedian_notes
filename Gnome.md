

## Set Hotkeys
---
- switch to workspace
	- https://askubuntu.com/questions/1205510/setting-keyboard-shortcuts-to-additional-workspaces
	```bash
	gsettings set org.gnome.desktop.wm.keybindings switch-to-  workspace-5 "['<Ctrl>5']"
	```
- move current window to different workspace
	- https://askubuntu.com/questions/1423846/how-can-i-add-shortcuts-to-move-windows-to-workspace-5-and-above
	```bash
	gsettings set "org.gnome.desktop.wm.keybindings" "move-to-workspace-5" "['<Super><Shift>h']" 

	```