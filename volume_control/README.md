# Audio on the T420
## Dependencies
```
sudo pacman -S alsa-utils
sudo pacman -S xbindkeys
```
## Necessary Files
```
~/.xbindkeysrc
```
## Needed Lines
```
# Place this in ~/.xbindkeysrc
# Mute Toggle
"amixer set Master toggle"
	m:0x0 + c:121
# Decrease Volume
"amixer set Master 5%-"
	m:0x0 + c:122
# Increase Volume
"amixer set Master 5%+"
	m:0x0 + c:123
```
## Reload Key Configuration
```
# Place this in ~/.bash_profile
xbindkeys --poll-rc
```
## Helpful Program
This program tells you what values each key returns. For example, when the mute button
is pressed, it returns `m:0x0 + c:121`.
```
xbindkeys --key
```

