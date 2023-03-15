# ArcoLARBS

![A beautiful ArcoLARB screenshot](img/pic-full-230315-0834-54.png)

<br>

### Table of Contents

1. [Introduction](#Introduction)
2. [Installation](#Installation)
3. [Post-Install](#Post-Install)
4. [Keybindings](#Keybindings)
5. [Links](#Links)

<br>

### Introduction

Don't want to deal with installing [Arch Linux](https://archlinux.org/)? Don't want to spend [forever configuring](https://www.youtube.com/watch?v=gCRzng7LsQI) every little aspect of your Linux build? Want to post screenshots to [r/unixporn](https://www.reddit.com/r/unixporn/)? Then ArcoLARBS is for you! 

ArcoLARBS is an easy to install linux operating system (well, not technically an operating system, but who cares, right?). Built on [ArcoLinux](https://arcolinux.com/) (a derivative of [Arch](https://archlinux.org/)) and configured using [Luke Smith's Auto-Bootstrapping Script (LARBS)](https://larbs.xyz/), ArcoLARBS is almost entirely the work of other people. But I'm lazy and I don't want to reinvent the wheel (read: reinstall and configure Arch for the hunderdth time), so here we are.

ArcoLARBS can be installed in about 20 minutes, customized in about five, and before you know it you'll be posting those sweet screenshots to [r/unixporn](https://www.reddit.com/r/unixporn/). Because that's why we're really here, right?

<br>

### Installation

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

### Post-Install (Optional)

Adding a custom wallpaper and corresponding colorscheme is simple with ArcoLARBS.

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

### Links 


 

 
