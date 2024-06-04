### Adding plugins
#### Dragon
- https://github.com/sxyazi/yazi/discussions/327
- add the following code in keymap.toml file
```toml
{ on = [ "<C-n>" ], run = '''
    shell 'dragon -x -i -T "$1"' --confirm
''' },
```