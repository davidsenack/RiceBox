# RiceBox

![A beautiful RiceBox desktop](screenshots/keycap_apps.png)
<br>

## Table of Contents

1. [Introduction](#Introduction)
2. [Themes](#Themes)
	1. [Arch Purple](#Arch-Purple)
4. [Installation](#Installation)
5. [Post-Install](#Post-Install(Optional))
6. [Keybindings](#Keybindings)
    1. [Basic Commands](#Basic-Commands)
    2. [Window Layouts](#Window-Layouts)
    3. [Basic Programs](#Basic-Programs)
    4. [Tags/Workspaces](#Tags/Workspaces)
    5. [System](#System)
    6. [Audio](#Audio)
    7. [Recording](#Recording)
7. [Links](#Links)
<br>

## Introduction

Don't want to deal with installing [Arch Linux](https://archlinux.org/)? Don't want to spend [forever configuring](https://www.youtube.com/watch?v=gCRzng7LsQI) every little aspect of your Linux build? Want to post screenshots to [r/unixporn](https://www.reddit.com/r/unixporn/)? Then RiceBox is for you!

RiceBox is an easy to install Linux operating system (well, technically a set of configuration scripts on top of an OS). Built on [ArcoLinux](https://arcolinux.com/) (a derivative of [Arch](https://archlinux.org/)) and configured using [Luke Smith's Auto-Rice Bootstrapping Scripts (LARBS)](https://larbs.xyz/), RiceBox is almost entirely the work of other people. But I'm lazy and don't want to reinvent the wheel.

So, what's the point of all of this? I grew tired of installing various Linux distros from the ground up and spending hours configuring everything. It's fun for a while, but I just want a system that works and has some advanced workflow options preconfigured. Sure, I could just save my dotfiles to Github or something like that, but I wanted something even more simple. Something everyone could use. Something I could use to post those sweet screenshots to [r/unixporn](https://www.reddit.com/r/unixporn/). Because that's why we're really here, right?
<br>

## Themes

### Arch Purple
![Arch Purple Desktop](screenshots/archpurple_desktop.png)
![Arch Purple Desktop](screenshots/archpurple_apps.png)

### X-Ray
![X-ray Desktop](screenshots/xray_desktop.png)
![X-ray Desktop](screenshots/xray_apps.png)

### Forest
![Forest Desktop](screenshots/forest_desktop.png)
![Forest Desktop](screenshots/forest_apps.png)

### Rust
![Rust Desktop](screenshots/rust_desktop.png)
![Rust Desktop](screenshots/rust_apps.png)

### Pink Japan
![Pink Japan Desktop](screenshots/pinkjp_desktop.png)
![Pink Japan Desktop](screenshots/pinkjp_apps.png)

### Nah
![Nah Desktop](screenshots/nah_desktop.png)
![Nah Desktop](screenshots/nah_apps.png)

### Keycap
![Keycap Desktop](screenshots/keycap_desktop.png)
![Keycap Desktop](screenshots/keycap_apps.png)

### I Use Arch BTW
![I Use Arch BTW Desktop](screenshots/iusearchbtw_desktop.png)
![I Use Arch BTW Desktop](screenshots/iusearchbtw_apps.png)

### Space
![Space Desktop](screenshots/space_desktop.png)
![Space Desktop](screenshots/space_apps.png)

### Arch
![Arch Desktop](screenshots/arch_desktop.png)
![Arch Desktop](screenshots/arch_apps.png)

### Streets
![Streets Desktop](screenshots/streets_desktop.png)
![Streets Desktop](screenshots/streets_apps.png)


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

4. After install, update the system and install `feh` and `python-pywal`:
```
sudo pacman -Syyu
```
```
sudo pacman -S feh python-pywal
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

### Wallpapers and Colorthemes
Adding a custom wallpaper and corresponding colorscheme is simple with RiceBox.

1. To install a preconfigured wallpaper and theme simply download the installer script and run:
```
wget rbtheme.sh
```
```
rbtheme [1-10] # replace [1-10] with a number
```

2. Or, to install your own wallpaper and corresponding theme, run:
```
wal -i /path/to/wallpaper.img
```
<br>

### Oh My Zsh (Custom Zsh Configuration)
Additionally, I recommend installing [Oh My Zsh](https://ohmyz.sh/):
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
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

### ArcoLinux

- [ArcoLinux Homepage](https://arcolinux.com/)
- [ArcoLinuxD Downloads](https://sourceforge.net/projects/arcolinux/files/ArcoLinuxD/)
- [Erik Dubois ArcoLinuxD Base Install Video](https://www.youtube.com/watch?v=B6TpyG2tIV0)
- [DistroTube's ArcoLinux Review](https://www.youtube.com/watch?v=J5mkCQ5YnH4)

### Arch Linux
- [Arch Linux Homepage](https://archlinux.org/)
- [Arch Linux Wiki](https://wiki.archlinux.org/)
- [Upgrading Arch/Arco](https://wiki.archlinux.org/title/System_maintenance#Upgrading_the_system)

### Additional Software

- [Oh My Zsh](https://ohmyz.sh/)
- [Pywal](https://github.com/dylanaraps/pywal)
- [feh](https://wiki.archlinux.org/title/Feh)

### Misc.

- [r/unixporn](https://www.reddit.com/r/unixporn/)
