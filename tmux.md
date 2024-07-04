# Tmux Cheat Sheet

Tmux is a terminal multiplexer, allowing you to create, manage, and navigate multiple terminal sessions within a single window. Here is a cheat sheet with the most useful tmux commands.

## Starting tmux

### Start a new session
```sh
tmux
```
or
```sh
tmux new-session -s <session-name>
```

### Attach to an existing session
```sh
tmux attach -t <session-name>
```

### List sessions
```sh
tmux ls
```

### Kill a session
```sh
tmux kill-session -t <session-name>
```

## Basic Key Bindings

By default, `Ctrl+b` is the prefix key for tmux commands. Press `Ctrl+b` and then the following keys:

### Session Management

- `d`: Detach from the current session
- `(`: Switch to the previous session
- `)`: Switch to the next session
- `s`: List and select sessions

### Window Management

- `c`: Create a new window
- `w`: List windows
- `n`: Move to the next window
- `p`: Move to the previous window
- `,`: Rename the current window
- `&`: Kill the current window

### Pane Management

- `"`: Split the window horizontally
- `%`: Split the window vertically
- `o`: Toggle between panes
- `x`: Kill the current pane
- `;`: Toggle between last active panes
- `z`: Toggle pane zoom
- `q`: Show pane numbers (followed by the number to switch to that pane)

### Resizing Panes

- `Ctrl+b` then `Ctrl+arrow`: Resize pane in the direction of the arrow

### Synchronize Panes
Enable synchronization across all panes in a window:
```sh
tmux setw synchronize-panes on
```
Disable synchronization:
```sh
tmux setw synchronize-panes off
```

### Copy Mode

- `[`: Enter copy mode
- `Space`: Begin selection (in copy mode)
- `Enter`: Copy selection (in copy mode)
- `q`: Quit copy mode
- `]`: Paste the copied buffer

### Miscellaneous

- `t`: Show the time
- `?`: List all key bindings
- `:`: Enter the command prompt to execute tmux commands directly

## Configuration File (`~/.tmux.conf`)

Here are some common configurations you might add to your `.tmux.conf` file:

### Set Prefix Key
```sh
set -g prefix C-a
unbind C-b
bind C-a send-prefix
```

### Enable Mouse Support
```sh
set -g mouse on
```

### Set Pane Base Index
```sh
set -g pane-base-index 1
```

### Customize Status Bar
```sh
set -g status-bg black
set -g status-fg white
set -g status-left '[#S] '
set -g status-right '%H:%M:%S %d-%b-%Y'
```

### Enable Vi Mode in Copy Mode
```sh
setw -g mode-keys vi
```

## Advanced Commands

### Rename Session
```sh
tmux rename-session -t <old-name> <new-name>
```

### Move Pane to Different Window
```sh
tmux move-pane -s <source-pane> -t <target-window>
```

### Source Configuration File
```sh
tmux source-file ~/.tmux.conf
```

## Tips

- **Using Prefix Key Efficiently:** Since the default prefix key `Ctrl+b` can be cumbersome, many users remap it to `Ctrl+a` (as shown in the configuration file section).
- **Pane Navigation:** Use `Ctrl+b` followed by arrow keys or `q` followed by the pane number for quick navigation.
- **Persistent Sessions:** Utilize tmux for long-running tasks or when you need to maintain your working environment across different connections or reboots.

