## nv: Run neovim like Midnight Command

```
# nv uses nvim to run as a file explorer
#!/bin/zsh
: If it's an existing file open in read only view and quit
[ -f $1 ] && nvim -R $1 && exit
: If it's an existing directory open it read only view and quit
[ -d $1 ] && nvim -c 'execute ":Ex"' -R $1 && exit
: Whatever, just open in read-only view
[ -d $1 ] && nvim -c 'execute ":Ex"' -R 
```

