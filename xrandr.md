list monitors
```bash
xrandr --listmonitors
```
connect external display in HDMI port
- mirror - primary  off
```bash
	xrandr --output eDP-1-1 --off;
	xrandr --output HDMI-1-2 --mode 1920x1080 --auto;
```
- mirror - both display ON
```bash
	xrandr --output eDP-1-1 --mode 1920x1080 --primary;
	xrandr --output HDMI-1-2 --mode 1920x1080 --auto;
```
- join display - to right
```bash
	xrandr --output eDP-1-1 --mode 1920x1080 --output HDMI-1-2 --mode 1920x1080 --right-of eDP-1-1;
```