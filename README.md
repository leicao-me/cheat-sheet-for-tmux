Cheat sheet for tmux
--------------------

  For my little brains. <br/>
  Seokju modified on 17.12.26

### Out session (@ original shell)

| action | command |
| ------ | ------- |
| create session | `tmux new -s [session-name]` |
| kill session | `tmux kill-session -t [session-name]` |
| attach session | `tmux attach -t [session-name]` |
| rename session | `tmux rename-session -t [old-name] [new-name]` |
| list session | `tmux ls` |

### In session 

| action | command |
| ------ | ------- |
| create window | `^b + c` |
| rename window | `^b + ,` |
| navigate window | `^b + n` <br/> `^b + p` <br/> `^b + l` <br/> `^b + [window-num]`|
| terminate window | `^b + &` <br/> `tmux kill-window -t [window-num]` |
| detach session | `^b + d` |
| help | `^b + ?` |

### In window / pane

| action | command |
| ------ | ------- |
| split pane | `^b + %` <br/> `^b + "` |
| delete pane | `^b + x` <br/> `^d` (no warning) |
| select pane | `^b + arrow_key` |
| resize pane | `^b + <M-arrow_key>` |

Color
-----
### color code 
  * dump color code by [dumpTmuxColor](https://gist.github.com/wecanspeak/7956277)
  ![tmux color code](https://raw.github.com/wecanspeak/cheat-sheet-for-tmux/master/tmux-color-code.png)
  

### fix vim in tmux color problem
  * add `export TERM=xterm-256color` in `~/.bashrc`
  * add `set t_ut=` in `~/.vimrc`
  * add `setw -g xterm-keys on` and  `set -g default-terminal "screen-256color"` in `~/.tmux.conf`

Reference
---------

* [Fixing Vim's Background Color Erase for 256-color tmux and GNU screen](http://sunaku.github.io/vim-256color-bce.html)
  



