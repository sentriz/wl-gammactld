### example [swaywm](https://github.com/swaywm/sway/) config

```
set $mode_colour "colour mode: gamma [o|p], brightness [k|l], contrast [n|m]"
mode $mode_colour {
    bindsym o exec "echo 'gamma -0.2' > /tmp/wl-gammactld"
    bindsym p exec "echo 'gamma +0.2' > /tmp/wl-gammactld"
    bindsym k exec "echo 'brightness -0.2' > /tmp/wl-gammactld"
    bindsym l exec "echo 'brightness +0.2' > /tmp/wl-gammactld"
    bindsym n exec "echo 'contrast -0.2' > /tmp/wl-gammactld"
    bindsym m exec "echo 'contrast +0.2' > /tmp/wl-gammactld"
    bindsym Return mode "default"
    bindsym Escape mode "default"
}
bindsym $super+c mode $mode_colour
exec wl-gammactld
```
