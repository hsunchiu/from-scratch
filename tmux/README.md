# Tmux 

## Install in Macos

```shell
brew install tmux
```

## Basic

Session, Window, And Panes.
![Windows and Pannel](https://media.beehiiv.com/cdn-cgi/image/fit=scale-down,format=auto,onerror=redirect,quality=80/uploads/asset/file/f2a2b9f8-d7d9-4ebe-90e8-5551b1c27e99/tmuxnesting.png)

Basically, tmux sessions have windows, and windows have panes. Here’s how I conceptualize the structure.
Sessions are for an overall theme, such as work, or experimentation, or sysadmin.
Windows are for projects within that theme. So perhaps within your experimentation session you have a window titled noderestapi, and one titled lua sample.
Panes are for views within your current project. So within your sysadmin session, which has a logs window, you may have a few panes for access logs, error logs, and system logs.

### Sessions
```shell
tmux new-session -s [session-nanme]
tmux attach -t [session-name]
tmux kill-session -t [session-name]
```
### Shortcut
These all play off of the ctrl-b shortcut.

#### Basics
? get help

#### Session management
s list sessions

$ rename the current session

d detach from the current session

#### Windows
c create a new window

, rename the current window

w list windows

% split horizontally

" split vertically

n change to the next window

p change to the previous window

0 to 9 select windows 0 through 9

#### Panes
% create a horizontal pane

" create a vertical pane

h move to the left pane. *

j move to the pane below *

l move to the right pane *

k move to the pane above *

q show pane numbers

o toggle between panes

} swap with next pane

{ swap with previous pane

! break the pane out of the window

x kill the current pane

## More

1. [https://hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/](https://hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/)

2. [https://www.ruanyifeng.com/blog/2019/10/tmux.html](https://www.ruanyifeng.com/blog/2019/10/tmux.html)

3. [https://linuxize.com/post/getting-started-with-tmux/](https://linuxize.com/post/getting-started-with-tmux/)

4. [https://danielmiessler.com/p/tmux/](https://danielmiessler.com/p/tmux/)
