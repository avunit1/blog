+++
title = "Arch Linux Speedrunning"
date = "2022-08-05"
author = "Avunit"
description = "What even is this?"
+++

Arch Linux speedrunning is basically installing arch linux from scratch as fast as possible.
There are some rules, such as:

- Don't fetch and use a script (or, for that matter, don't download anything that is not from official Arch Linux repositories) (though you are allowed to write down a script from scratch once you start).
- The time taken to download each package, from the moment the loading bar appears to the moment the screen scrolls down to a new line, is cut out from the final time.

My PB is 2:05, which is relatively good. The current WR is being held by [this guy]([https://www.youtube.com/watch?v=5X9TWW8lXd0]): It's impressive to say the least.

The commands i used were:

- cfdisk
- mkfs.xfs /dev/sda1
- mount /dev/sda1 /mnt
- pacman -Sy tmux
- tmux
- pacstrap /mnt base linux
- genfstab /mnt>/mnt/etc/fstab;arch-chroot /mnt bash -c 'pacman -Sy grub;grub-install /dev/sda;grub-mkconfig -o /boot/grub/grub.cfg';reboot

After typing the cfdisk command, select the DOS partition option, create a new partition using all of the available space. Make sure you make it UN-BOOTABLE, then write changes to disk, and exit. After this, input the rest of the commands as following.

A speedrun using the commands i used can be seen [here]([https://www.youtube.com/watch?v=8utpbbdj0LQ]).

After all, it's a pretty dumb achievement but it's something to brag about to linux users.
