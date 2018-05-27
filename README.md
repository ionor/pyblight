# pyblight

A program that simplifies setting keyboard and screen brightness. Can be useful if you run a window manager that doesn't set these things for you and you want to bind hotkeys.

Uses the kernels /sys files to extract and to change values.

Works with percentages so the value should be either a fixed percentage or a change.

## INSTALLATION
Requires python 3 and for unprivileged users you need to make sure that the relevant files in sys are writeable. 

Two preconfigured udev rules files are included as an example but may need to be modified. Most likely just makeing sure that the correct group and path is set.

## USAGE

### Syntax

pyblight [device] [action] [value]  
[device]  
display  
keyboard  
  
[actions]  
get           - get current value  
set           - set new value  
  
[value]  
+X            - increase backlightning  
-X            - decrease backlightning  
 X            - set fixed value. 0-100  
  

### Examples

* pyblight display set 40%
* pyblight display set +10%
* pyblight display get

or

* pyblight keyboard set 30%
* pyblight keyboard set -10%
* pyblight keyboard get 

## TODO
- make things less hardcoded and allow setting things in configuration files. 
