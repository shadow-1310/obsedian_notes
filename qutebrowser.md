## Installation

### Debian/Ubuntu
- Clone the git repo
	- [official documentation](https://qutebrowser.org/doc/install.html#debian)
- install dependencies inside virtual env
	```bash
	python3 scripts/mkvenv.py
	```
- this qutebrowser is inside your directory so, you can't call it directly, so a script name 'qutebrowser' in $PATH, so that typing 'qutebrowser' in terminal will access, the wrapper script will be like following - 
```bash
#!/bin/bash
~/path/to/qutebrowser/.venv/bin/python3 -m qutebrowser "$@"
```


- [selecting text](https://www.reddit.com/r/qutebrowser/comments/f5a7oj/selecting_text_in_qutebrowser/)

opening a new link
https://github.com/qutebrowser/qutebrowser/issues/922
- as I have a wrapper script in my bin which calls qutebrowser in my virtualenv, so this can't have access to the flags I pass (letter I got to know "$@" may take the flags)
- so directly use path to qutebrowser installation as browser like the following in [[newsboat]] config
```bash
browser "~/softwares/qutebrowser/qutebrowser/.venv/bin/python3 -m qutebrowser --target window"
```