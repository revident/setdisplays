# setdisplays

A shell script to manage multiple monitor layouts of a laptop that moves from place to place.

Design Goals:

* Enable quick switching to known/desired layouts.
  * Drop into new equipment at a hot desk or presentation.
  * The Desktop Environment fails to recover previously seen monitor layout.

# Adapting this script

Different hardware and driver combinations will produces various names for 
your Display outputs. Start by having only your default display on. And then 
add additional monitors/projects to understand which physical output matches 
which name.

```
[revident@host1 ~]$ xrandr 
Screen 0: minimum 320 x 200, current 1920 x 1080, maximum 8192 x 8192
DP-1 disconnected (normal left inverted right x axis y axis)
HDMI-1 connected primary 1920x1080+0+0 (normal left inverted right x axis y axis) 531mm x 299mm
   1920x1080     60.00*+  50.00    59.94  
   1920x1080i    60.00    50.00    59.94  
   1600x1200     60.00  
   1680x1050     59.88  
   1280x1024     75.02    60.02  
   1440x900      59.90  
   1280x960      60.00  
   1152x864      75.00  
   1280x720      60.00    50.00    59.94  
   1024x768      75.03    70.07    60.00  
   832x624       74.55  
   800x600       72.19    75.00    60.32    56.25  
   720x576       50.00  
   720x480       60.00    59.94  
   640x480       75.00    72.81    66.67    60.00    59.94  
   720x400       70.08  
DP-2 disconnected (normal left inverted right x axis y axis)
HDMI-2 disconnected (normal left inverted right x axis y axis)
DP-3 disconnected (normal left inverted right x axis y axis)
HDMI-3 disconnected (normal left inverted right x axis y axis)
```
## Debugging

There is a debugging function to help you see what a giving profile will look 
like without making changes to your monitor layout.

```
SETDISPLAYS_DBG=1; setdisplays default
```

# Resources
* [RandR @ Wikipedia](https://en.wikipedia.org/wiki/RandR)
* [xrandr @ ArchWiki](https://wiki.archlinux.org/index.php/Xrandr)
* [XRandR @ x.org](https://www.x.org/wiki/Projects/XRandR/)
