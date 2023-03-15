# ArcoLARBS

Don't want to deal with installing Arch Linux? Don't want to spend forever configuring every little aspect of your linux build? Want to post screenshots to r/unixporn? Then ArcoLARBS is for you! 

ArcoLARBS is an easy to install linux operating system (well, not technically but who cares, right?). Built on ArcoLinux (a derivative of Arch) and configured using Luke Smith's Auto-Bootstrapping Script (LARBS), ArcoLARBS is almost entirely the work of other people. But I'm lazy and I don't want to reinvent the wheel (read: reinstall and configure Arch for the hunderth time) and so here we are.

ArcoLARBS can be installed in about 10 minutes, customized in about five, and before you know it you'll be posting those sweet screenshots to r/unixporn. Because that's why we're really here, right?

### Installation

First, we need to download the ArcoLinuxD iso image:

` $ wget https://sourceforge.net/projects/arcolinux/files/ArcoLinuxD/arcolinuxd-v23.03.01-x86_64.iso/download `

Next, we need to write our iso image to a bootable media device. In our case, we'll be using the linux utility `dd`, but you could also use something like [BalenaEtcher](https://www.balena.io/etcher). If using `dd` ensure that you are writing to the correct block device. You can list block devices with `$ lsblk`. In our case we're writing to `/dev/sdb`, your device may be different!

` $ dd if=arcolinuxd-v23.03.01-x86_64.iso of=/dev/sdb `




 

 
