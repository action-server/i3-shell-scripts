# i3-modular-config
This script allows you to seperate your i3 config into multiple sub configs.

## Usage

1. Add your sub configs to the following directory: `$XDG_CONFIG_HOME/i3/configs`
2. Add the name of each sub config separated by a new line to the following file: `$XDG_CONFIG_HOME/i3/data/list`
3. Replace your reload bind with the following line:
```
bindsym --release $mod+Shift+r exec --no-startup-id i3-modular-config
```
4. Run i3-modular-config

> Tip: Make sure that the script can be found in your $PATH.
## Example
### File tree
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
### Contents of ~/.config/i3/data/list
```
main.config
float.config
bind.config
app.config
mode.config
gap.config
bar.config
```
