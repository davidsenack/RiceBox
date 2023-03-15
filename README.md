# RiceBox

![A beautiful ArcoLARB screenshot](img/pic-full-230315-0834-54.png)
<br>

## Table of Contents

1. [Introduction](#Introduction)
2. [Installation](#Installation)
3. [Post-Install](#Post-Install(Optional))
4. [Keybindings](#Keybindings)
    1. [Basic Commands](#BasicCommands)
    2. [Window Layouts](#WindowLayouts)
    3. [Basic Programs](#BasicPrograms)
    4. [Tags/Workspaces](#Tags/Workspaces)
    5. [System](#System)
    6. [Audio](#Audio)
    7. [Recording](#Recording)
5. [Links](#Links)
<br>

## Introduction

Don't want to deal with installing [Arch Linux](https://archlinux.org/)? Don't want to spend [forever configuring](https://www.youtube.com/watch?v=gCRzng7LsQI) every little aspect of your Linux build? Want to post screenshots to [r/unixporn](https://www.reddit.com/r/unixporn/)? Then RiceBox is for you! 

RiceBox is an easy to install linux operating system (well, not technically an operating system, but who cares, right?). Built on [ArcoLinux](https://arcolinux.com/) (a derivative of [Arch](https://archlinux.org/)) and configured using [Luke Smith's Auto-Bootstrapping Script (LARBS)](https://larbs.xyz/), RiceBox is almost entirely the work of other people. But I'm lazy and I don't want to reinvent the wheel (read: reinstall and configure Arch for the hunderdth time), so here we are.

RiceBox can be installed in about 20 minutes, customized in about five minutes, and before you know it you'll be posting those sweet screenshots to [r/unixporn](https://www.reddit.com/r/unixporn/). Because that's why we're really here, right?
<br>

## Installation

1. Download the ArcoLinuxD iso image:
```
wget https://sourceforge.net/projects/arcolinux/files/ArcoLinuxD/arcolinuxd-v23.03.01-x86_64.iso/download
```
<br>

2. Write the iso image to a bootable media device. In this case, we'll be using the Linux utility `dd`. Make sure to substitute `of=/dev/sdb` with the correct block device! 
```
dd if=arcolinuxd-v23.03.01-x86_64.iso of=/dev/sdb
```
<br>

3. Follow the ArcoLinuxD install directions at [www.arcolinuxd.com](https://www.arcolinuxd.com/installation/) or [watch this video](https://www.youtube.com/watch?v=B6TpyG2tIV0) for a walkthrough of the ArcoLinuxD base install process.
<br>

4. After install, update the system:
```
sudo pacman -Syyu
```
<br>

5. Install [Luke's Auto-Rice Bootstrapping Scripts (LARBS)](https://larbs.xyz). Simply download and run the script and follow the instructions in the installer:

```
curl -LO larbs.xyz/larbs.sh
```
```
sh larbs.sh
```
<br>

6. Reboot the system:
```
sudo reboot now
```
<br>

## Post-Install (Optional)

Adding a custom wallpaper and corresponding colorscheme is simple with RiceBox.

1. Download a wallpaper and set it as the background. Replace 'wallpaper.jpg' with the appropriate links: 
```
wget wallpaper.jpg
```
``` 
setbg /path/to/wallpaper.jpg
```
<br>

2. To generate a custom colorscheme based on your wallpaper, install and run `wal`:
```
sudo pacman -S python-pywal
```
```
wal -i /path/to/wallpaper.jpg
```
<br>

## Keybindings

Default keybindings per Luke's Auto-Ricing Bootloader Script. Checkout [LARBS docs](https://larbs.xyz/larbs-dwm.pdf) for more info. 

### DWM Commands

- `Mod+Enter` – Spawn terminal (the default terminal is st; run man st for more.)
- `Mod+q` – Close window 
- `Mod+d` – dmenu (For running commands or programs without shortcuts) 
- `Mod+j/k` – Cycle thru windows by their stack order 
- `Mod+Space` – Make selected window the master (or switch master with 2nd)
- `Mod+h/l` – Change width of master window 
- `Mod+z/x` – Increase/decrease gaps (may also hold Mod and scroll mouse) 
- `Mod+a` – Toggle gaps 
- `Mod+A` – Gaps return to default values (may also hold Mod and middle click) 
- `Mod+Shift+Space` – Make a window float (move and resize with Mod+left/right click). 
- `Mod+s` – Make/unmake a window “sticky” (follows you from tag to tag) 
- `Mod+b` – Toggle statusbar (may also middle click on desktop) 
- `Mod+v` – Jump to master window 
<br>

### Window Layouts

- `Mod+t` – Tiling mode (active by default)
- `Mod+T` – Bottom stack mode (just like tiling, but master is on top)
- `Mod+f` – Fullscreen mode
- `Mod+F` – Floating (AKA normie) mode
- `Mod+y` – Fibonacci spiral mode
- `Mod+Y` – Dwindle mode (similar to Fibonacci)
- `Mod+u` – Master on left, other windows in monocle mode
- `Mod+U` – Monocle mode (all windows fullscreen and cycle through)
- `Mod+i` – Center the master window
- `Mod+I` – Center and float the master window
- `Mod+o/O` – Increase/decrease the number of master windows
<br>

### Basic Programs

- `Mod+r` – lf (file browser/manager)
- `Mod+R` – htop (task manager, system monitor that Redditors use to look cool)
- `Mod+e` – neomutt (email) – Must be first configured by running mw add.
- `Mod+E` – abook (contacts, addressbook, emails)
- `Mod+m` – ncmpcpp (music player)
- `Mod+w` – Web browser (LibreWolf by default)
- `Mod+W` – nmtui (for connecting to wireless internet)
- `Mod+n` – vimwiki (for notes)
- `Mod+N` – newsboat (RSS feed reader)
- `Mod+F4` – pulsemixer (audio system control)
- `Mod+Shift+Enter` – Show/hide dropdown terminal
- `Mod+’` – Show/hide dropdown calculator
- `Mod+D` – passmenu (password manager)
<br>

### Tags/Workspaces

There are nine tags, active tags are highlighted in the top left.
- `Mod+(Number)` – Go to that number tag
- `Mod+Shift+(Number)` – Send window to that tag
- `Mod+Tab` – Go to previous tag (may also use \ for Tab)
- `Mod+g` – Go to left tag (hold shift to send window there)
- `Mod+;` – Go to right tag (hold shift to send window there)
- `Mod+Left/Right` – Go to another display
- `Mod+Shift+Left/+Right` – Move window to another display
<br>

### System

- `Mod+BackSpace` –Choose to lock screen, logout, shutdown, reboot, etc.
- `Mod+F1` – Show this document
- `Mod+F2` – Watch tutorial videos on a subject
- `Mod+F3` – Select screen/display to use
- `Mod+F4` – pulsemixer (audio control)
- `Mod+F6` – Transmission torrent client (not installed by default)
- `Mod+F7` – Toggle on/off transmission client via dmenu
- `Mod+F8` – Check mail, if mutt-wizard is configured. (Run mw add to set up.)
- `Mod+F9` – Mount a USB drive/hard drive or Android
- `Mod+F10` – Unmount a non-essential drive or Android
- `Mod+F11` – View webcam
- `Mod+F12` – Rerun keyboard mapping scripts if new keyboard is attached
- `Mod+‘` – Select an emoji to copy to clipboard
- `Mod+Insert` – Show contents of clipboard/primary selection
<br>

### Audio

I use ncmpcpp as a music player, which is a front end for mpd.
- `Mod+m` – ncmpcpp, the music player
- `Mod+.` – Next track
- `Mod+,` – Previous track
- `Mod+<` – Restart track
- `Mod+>` – Toggle playlist looping
- `Mod+p` – Toggle pause
- `Mod+p` – Force pause music player daemon and all mpv videos
- `Mod+M` – Mute all audio
- `Mod+-` – Decrease volume (holding shift increases amount)
- `Mod++` – Increase volume (holding shift increases amount)
- `Mod+[` – Back 10 seconds (holding shift moves by one minute)
- `Mod+]` – Forward 10 seconds (holding shift moves by one minute)
- `Mod+F4` – pulsemixer (general audio/volume sink/source control)
<br>

### Recording

I use maim and ffmpeg to make different recordings of the desktop and audio. All of these
recording shortcuts will output into ˜, and will not overwrite previous recordings as their names
are based on their exact times.
- `PrintScreen` – Take a screenshot
- `Shift+PrintScreen` – Select area to screenshot
- `Mod+PrintScreen` – Opens dmenu menu to select kind of audio/video recording
- `Mod+Delete` – Kills any recording started in the above way
- `Mod+Shift+c` – Toggles a webcam in the bottom right for screencasting
- `Mod+ScrollLock` – Toggle screenkey (if installed) to show keypresses
<br>

## Links 

### LARBS

- [Luke's Auto-Rice Bootstrapping Scripts (LARBS](https://larbs.xyz/)
- [A Friendly Guide to LARBS](https://larbs.xyz/larbs-dwm.pdf)
- [Luke's YouTube channel](https://youtube.com/lukesmithxyz)
- [LARBS Github Page](https://github.com/lukesmithxyz/voidrice)

### ArcoLinux | Arch Linux

- [ArcoLinux Homepage](https://arcolinux.com/)
- [ArcoLinuxD Downloads](https://sourceforge.net/projects/arcolinux/files/ArcoLinuxD/)
- [Erik Dubois ArcoLinuxD Base Install Video](https://www.youtube.com/watch?v=B6TpyG2tIV0)
- [DistroTube's ArcoLinux Review](https://www.youtube.com/watch?v=J5mkCQ5YnH4)
<br>

- [Arch Linux Homepage](https://archlinux.org/)
- [Arch Linux Wiki](https://wiki.archlinux.org/)
- [Upgrading Arch/Arco](https://wiki.archlinux.org/title/System_maintenance#Upgrading_the_system)

 

 
