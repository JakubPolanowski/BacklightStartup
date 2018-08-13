# BacklightStartUp

A helper script for xbacklight that keeps tracks of monitor brightness, useful for keep brightness levels the same between sessions. 

This script retains brightness levels within a file called "backlight" in .script_memory within the home directory (everything gets created automatically if directory and/or file does not exist).

# Installation 

## Dependencies 

* `xbacklight` (often comes pre-installed for most distros)
* `python3`

## Installing

Simply make the script executable, this can be done via `sudo chmod a+x BacllightStartUp`

#Usage

The purpose of this script is to be used as part of a Window Manager configuration. Although it can be used in a terminal, there would be no advantage to use it over `xbacklight`

The recommended use is to have it be executed when the Window Manager starts up, specifically `BacklightStartUp -l` which will set the brightness to the last stored level. It can be used with hotkeys to increase brightness up and down, storing the current value.

### Syntax:
`BacklightStartUp -option value`

### Options:

`-h` - Help
`-l` - Launch, requires 0-100 fallback value, if no previous brightness level is saved, sets to fallback value
`-i` : Increase, increases brightness and stores the increased level

### Mechanism 

This script simply stores and updates a text file `~/.script_memory/mon_backlight.txt`, which is then used when read from when the `-l` or launch is used. 
