# pyblight

A program that simplifies setting keyboard and screen brightness. Can be useful if you run a window manager that doesn't set these things for you and you want to bind hotkeys.

Uses the kernels /sys files to extract and to change values.

Works with percentages so the value should be either a fixed percentage or a change.

## INSTALLATION
Requires python 3 and for unprivileged users you need to make sure that the relevant files in sys are writeable. 

Two preconfigured udev rules files are included as an example but may need to be modified. Most likely just makeing sure that the correct group and path is set.

## CONFIGURATION
pyblight looks for a config-file in $HOME/.config/pyblight or in /etc/xdg/pyblight (in that order). 

Currently there are two configurables as shown in the default config file below. 
  
[Main]  
display_backlight = "/sys/class/backlight/intel_backlight/"  
keyboard_backlight = "/sys/class/leds/smc::kbd_backlight/"  
  
## USAGE

### Syntax

pyblight [device] [action] [value] [optionals]

[device]  
   display  
   keyboard  

[actions]  
   get                           - get current value  
   set                           - set new value  
  
[value]  
   +X                            - increase backlightning  
   -X                            - decrease backlightning  
    X                            - set fixed value. 0-100  
  
[optionals]  
    --dont-store                 - set value but dont store  

Other alternatives  
   usage                         - show this text  
   version                       - shows version and exits  
   restore                       - restores previous value  
   store                         - stores current value  
 
