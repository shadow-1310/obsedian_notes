## Problems
#### Multi Monitors
- When in one monitor a window is made fullscreen, in the other monitor windows does not stay transparent, they become opaque
	- solution is the config file parameter. In the config file there is a parameter called **unredir-if-possible = true;**
	- if it is set to true compositer does not work on other windows to save resources
	- it is usefull while gaming, as game window is made fullscreen, the compositor save resources
	- Solution is to set the parameter as false 
	```txt
	unredir-if-possible = false;
	```

