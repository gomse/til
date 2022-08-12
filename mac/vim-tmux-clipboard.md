[Vim&Tmux에서 Mac/Linux 클립보드 사용하기](https://rampart81.github.io/post/vim-clipboard-share/)

`.vimrc`:
```
set clipboard=unnamed "use OS clipboard
```

```
brew install reattach-to-user-namespace
```

`.tmux.conf`:
```
setw -g mode-keys vi
unbind -Tcopy-mode-vi Enter
bind-key -T copy-mode-vi 'v' send -X begin-selection
bind-key -T copy-mode-vi 'V' send -X select-line
bind-key -T copy-mode-vi 'r' send -X rectangle-toggle
bind -Tcopy-mode-vi 'y' send -X copy-pipe-and-cancel "reattach-to-user-namespace pbcopy"
```

