# Things to do with manjaro i3 + Thinkpad X1

## HiDPI

### set DPI in X Server

https://wiki.archlinux.org/index.php/x_resources

- `nano ~/.Xresources` to edit settings
- `xrdb -merge ~/.Xresources` to apply settings
- `[cmd+shift+r]` to reload i3 and see settings applied 

Just set to a multiple of the existing setting (base was 96x96)

read existing settings with:

- `xdpyinfo | grep dots`
- `xrdb -query | grep dpi`

## Trackpad

### add boot parameter

- `sudo nano /etc/default/grub`
- append `psmouse.synaptics_intertouch=1` to the `GRUB_CMDLINE_LINUX_DEFAULT=...` line
