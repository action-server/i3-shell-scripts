# i3-shell-scripts
A collection of useful shell scripts for i3wm

## i3-modular-config
This script allows you to seperate your i3 config into multiple sub configs.

### Usage

1. Add your sub configs to the following directory: `$XDG_CONFIG_HOME/i3/configs`
2. Add the name of each sub config separated by a new line to the following file: `$XDG_CONFIG_HOME/i3/data/list`
3. Replace your reload bind with the following line:
```
bindsym --release $mod+Shift+r exec --no-startup-id i3-modular-config
```
4. Run i3-modular-config

> Tip: Make sure that the script can be found in your $PATH.
### Example
#### File tree
```
~/.config/i3/
├── configs
│   ├── app.config
│   ├── bar.config
│   ├── bind.config
│   ├── float.config
│   ├── gap.config
│   ├── main.config
│   └── mode.config
└── data
    └── list
```

`~/.config/i3/data/list`
```
main.config
float.config
bind.config
app.config
mode.config
gap.config
bar.config
```

## i3-kill-wrapper
Wrapper script for the i3 kill command

### Usage
1. add the name of the windows you wish to persist, each separated by a new line to ~/.config/i3/data/persist.
2. Bind your prefered window kill key combo to this script.

## i3-auto-float
This scripts allows i3 to remember floating windows after closing them.

### Dependencies
[i3-modular-config](https://github.com/action-server/i3-modular-config) <br>
This dependency is needed for a clean setup

### Usage
1. [Setup i3-modular-config](https://github.com/action-server/i3-modular-config/blob/master/README.md/)
2. Create the following sub config: `~/.config/i3/configs/float.config`
3. Add the above sub config to the list of configs mentioned in the [i3-modular-config README](https://github.com/action-server/i3-modular-config/blob/master/README.md/)
4. Replace your floating toggle bind with the following line:
```
bindsym $mod+Shift+space exec --no-startup-id i3-auto-float
```
> Tip: Make sure that the script can be found in your $PATH.
