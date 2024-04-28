## Problems
- widget not showing wifi
	- [wlan not showing in widget](https://www.reddit.com/r/qtile/comments/1636458/widget_wlan_not_showing/)
	- problem is we have to define the interface in the parameter. we can get the interface name by either of the following commands
```bash
iwgetid

iwlist scan	
```
