It is a fork from https://github.com/TxGVNN/i3-config with more improvements: systems bars, more sensors, stock exchange rates, gold, silver(metal) rates, e-coins rates, etc. implementd with curl and  bash script over json files.

The screenshot show how my changes looks like with the new features added --> exchange rates, hardware  resources monitoring graphs, system, coins, etc.


# i3wm configuration files

I use Arch GNU/Linux.
```
$i3 --version
i3 version 4.18 (2020-02-17) © 2009 Michael Stapelberg and contributors
```
## Features

- Basic i3 configuration
- Show/hide fastly floating terminal (See bindings)
- Updating workspace name even working
- Create new workspace by naming (or moving container to new)
- Monitoring, you can put your bash scripts into `~/.i3/bin/{daemon.d,bar.d}`
- Reminder

## Setups
```
git clone https://github.com/flashlan/i3-config.git ~/.i3
```
Don't forget setup the `Xresources` file. If you expect more dotfiles,

## Bindings
* <kbd>Super</kbd>+<kbd>Enter</kbd> Open terminal
* <kbd>Super</kbd>+<kbd>d</kbd> Open dmenu
* <kbd>Super</kbd>+<kbd>Shift</kbd>+<kbd>e</kbd> System tools
* <kbd>Super</kbd>+<kbd>Shift</kbd>+<kbd>q</kbd> Close current container
* More basic bindings... (see `config`)
* <kbd>Super</kbd>+<kbd>f1</kbd> Toggle fastly floating terminal
* <kbd>Super</kbd>+<kbd>t</kbd> Rename workspace name (with workspace number)
* <kbd>Super</kbd>+<kbd>Shift</kbd>+<kbd>t</kbd> Rename workspace name
* <kbd>Super</kbd>+<kbd>i</kbd> Create new workspace by naming (Go to if already exists)
* <kbd>Super</kbd>+<kbd>Shift</kbd>+<kbd>i</kbd> Move a container to workspace by naming
* <kbd>Super</kbd>+<kbd>m</kbd> Mark a container
* <kbd>Super</kbd>+<kbd>Shift</kbd>+<kbd>m</kbd> Go to the marked container
* <kbd>Super</kbd>+<kbd>'</kbd> Reminder

### Mouse mode

* <kbd>Super</kbd>+<kbd>g</kbd> Go to mouse mode, after that you can

* <kbd>&larr;(a)</kbd>, <kbd>&rarr;(d)</kbd>, <kbd>&uarr;(w)</kbd>, <kbd>&darr;(x)</kbd> `Mouse move left, right, up & down`

* <kbd>q, e, c, z</kbd> `Move top+left, top+right, bottom+right, bottom+left`

* <kbd>$mod+(above)</kbd> `Mouse move faster (2*normal)`

* <kbd>Control+(above)</kbd> `Mouse move slower (normal/3)`

* <kbd>k</kbd>, <kbd>j</kbd>, <kbd>s</kbd>, <kbd>h</kbd>, <kbd>l</kbd> `Mouse click right, left, middle, wheel up, wheel down`

* <kbd>Shift+j</kbd> `It means Shift + Right click (mark feature)`

* <kbd>Control+h</kbd>, <kbd>Control+l</kbd> `It means Control + Right/Left click (zoom feature in browser)`

## Screenshots

It is a fork from https://github.com/TxGVNN/i3-config

The screenshot show how my changes looks like with the new features added --> exchange rates, hardware  resources monitoring graphs, system, coins, etc.

![The screenshot show how my changes look like with the new features add:](https://raw.githubusercontent.com/flashlan/i3-config/master/desktop.png)



## Packages
- required

``xinit xbacklight xinput i3blocks rxvt-unicode-256color screen feh scrot redshift alsa-utils acpi fonts-font-awesome xdotool
``
- optional

``wicd emacs ranger firefox
``

## Issues
- Icon not show?

>depends on fonts-font-awesome

- i3 crash caused by mark features?

>https://github.com/i3/i3/issues/2511

- If you want conky feature
>Enable conky configuration on `~/.i3/config`

```
exec --no-startup-id conky -d -c ~/.i3/conky-right
exec --no-startup-id conky -d -c ~/.i3/conky-left
```
