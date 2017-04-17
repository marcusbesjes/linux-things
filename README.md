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
*remember to uncomment this line, it's commented by default*

then restart logind
```
$ systemctl restart systemd-logind
```

## Setup

### Screens

- install ARandR `sudo apt-get instsall arandr`
- add `.screenlayout` to `$PATH`

### Keyboard

- when keys are weird: `setxkbmap us`

## Sublime

### Packages

- Themr (!)
- Schemr (!)
- Material Theme (nice theme)
  + run configuration to tweak it
- SideBarEnhancements (!)
- SyncedSideBar (?)
- sublime-github (!)
- SublimeLinter-contrib-standard (!)
- Markdown Preview (use with [LivePage chrome extention](https://chrome.google.com/webstore/detail/livepage/pilnojpmdoofaelbinaeodfpjheijkbh)) (!)
- MarkdownEditing
- Markdown Extended


## Notes

Things to add later

- to watch many files: echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
- sublime
  - sublime keybindings (indent paste) and settings (hide node_modules)
  - nice console.log solution
- terminator plugin for clicking files to open in editor with regex
- bluetooth reset fix https://gist.github.com/pylover/d68be364adac5f946887b85e6ed6e7ae
- 
