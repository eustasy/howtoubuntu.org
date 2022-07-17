---
title: How to Resize Partitions with the Ubuntu or GParted Live CD
breadcrumb: resize partitions live cd dvd usb gparted
excerpt: Having installed Ubuntu, you may find yourself wanting to shrink or get rid of your Windows partition completely. This tutorial will show you how do do either of those things, with a variety or filesystems, including NTFS, and EXT4. The instructions do not vary based on filesystem format.
---

Having installed Ubuntu, you may find yourself wanting to shrink or get rid of your Windows partition completely. This tutorial will show you how do do either of those things, with a variety or filesystems, including NTFS, and EXT4. The instructions do **not** vary based on filesystem format.

Consider disabling System Protection and Pagefile on Windows (if you are running out of space there too, both can use a lot of space but protect and speed up Windows).

Make a Backup of as much as possible if you have the space on an external drive, usb, or cd/dvd.

1. Boot either a [Ubuntu](https://www.ubuntu.com/download) or [GParted Live CD](https://gparted.org/livecd.php).
2. Open GParted.
3. Right-click on the partition you wish to shrink.
4. Select Resize.
5. Shrink or Delete the target partition (make sure you leave at least a couple of GB for an OS to play with, especially Windows, unless you're deleting it completely).
6. Click Apply (tick at the right of the icons along the top, this might take a while, and you can't undo or stop it half-way through).
7. Right-click on your Ubuntu Partition.
8. Expand into all the free space.
9. Click Apply again.

[![GParted is a nice way to Manage Partitions]({{ '/assets/images/how-to/resize-partitions-with-the-ubuntu-or-gparted-live-cd/Screenshot-from-2012-06-04-195206.png' | relative_url }})]({{ '/assets/images/how-to/resize-partitions-with-the-ubuntu-or-gparted-live-cd/Screenshot-from-2012-06-04-195206.png' | relative_url }})

This could take a fair while to shift things about, so make sure you're plugged in and don't shut a laptops lid (the Ubuntu Live CD will go to sleep). You may want to disable screen locking and sleeping after a certain time on the Ubuntu Live CD under Power Options.

If you have modified a partition containing Microsoft Windows, it might run a disk check when next started, this is normal behavior, it should finish and reboot. Boot into Windows before accessing the Windows partition from Ubuntu.

## Congratulations, you've successfully resized your partitions!
