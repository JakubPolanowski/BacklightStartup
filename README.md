# BacklightStartUp

A wrapper for xbacklight that keeps tracks of monitor brightness, useful for keep brightness levels the same between logins. This script retains brightness levels within a file called "backlight" in .script_memory within the home directory (everything gets created automatically if directory and/or file does not exist).

# Installtion 
Simply 'git clone' or download the zip, then make it executable via sudo chmod a+x

# Dependencies 
Requires xbacklight and python3 

#Usage
This is intended to be used in a config of a Window Manager, however it can also be used manually with a terminal.

The syntax of the command is:

BacklightStartUp -option value

Options are:

    -h : Help, Outputs information on usage 
    -l : Launch, requires a 0-100 value, if there is no previous brightness level saved, sets brightness to the value given, else brightness is set to the previously saved level
    -i : Increase, runs xbacklight -inc $value, increasing brightness by the given value then updates the "backlight" file with the new brightness level
    -d: Decrease, runs xbacklight -dec $value, decreasing brightness by the given value then update the "backlight" file with the new brightness level