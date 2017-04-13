# Just linux things

A bunch of stuff you have to / are able to do to make linux work (exactly like you want).

And by you I mean me.

## Settings

### Closing laptop lid should not hibernate

Since there might be a monitor connected and this doesn't affect the default behavior I'm disabling hibernate on lid closed.

edit `/etc/systemd/logind.conf`

put

```
HandleLidSwitch=ignore
```
*remember to uncomment*

then restart logind
```
$ systemctl restart systemd-logind
```

## Setup

### Screens

- `sudo apt-get instsall arandr`
- add `.screenlayout` to `$PATH`

### Keyboard

-
