# swaycmd - Get the CWD of the focued view
This script allows you to get the current working directory of the focused window/view. If the window/view is running inside xwayland the script simply falls back to [`xcwd`](https://github.com/schischi/xcwd), so that also needs to be installed.

This is useful if you want your terminal or other programs to open in the CWD of the curently focused window. 

## Dependencies

- `gron`
- `jq`
- `xcwd`

The script should work on both FreeBSD and Linux.

## Running
Add `swaycwd` to your `$PATH` and run it like this
```
$ swaycwd
/usr/home/qiu
```
Example sway config:

```
# Start a terminal in CWD
bindsym $mod+Shift+Return exec 'cd "$(swaycwd)" && st'
```
