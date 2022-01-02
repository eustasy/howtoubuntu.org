---
title: How to make your Dual Boot better with Burg
breadcrumb: burg
excerpt: Burg gives you the ability to use custom themes for selecting your bootloader, both with and without text. It also opens up the possibility of customizing and developing your own themes.
---

Grub 2 is all well and good, but if you want your dual boot to look a little better, then it's time to reverse it.

Burg gives you the ability to use custom themes for selecting your bootloader, both with and without text. It also opens up the possibility of customizing and developing your own themes.

## Warnings

Using the <span class="box">sudo</span> command, _especially_ when affecting your bootloader, can render your system unbootable. Read all instructions and confirm you understand before executing any commands. When pasting into the Terminal, use <span class="box">Ctrl</span>+<span class="box">Shift</span>+<span class="box">V</span>, NOT <span class="box">Ctrl</span>+<span class="box">V</span>.

## Installing

We need to add a couple of PPAs (that's a place for ubuntu to get software from), update the sources (so your computer knows they're there) and then install a few things.

```bash
sudo add-apt-repository ppa:n-muench/burg
sudo add-apt-repository ppa:danielrichter2007/grub-customizer
sudo apt install burg burg-themes grub-customizer
```

This will install 3 packages, <span class="box">burg</span> (that's the main one), <span class="box">burg-themes</span> (to make it look nice), and <span class="box">grub-customizer</span> (I know we're getting rid of grub and replacing it, but grub-customizer works for burg too).

You can search for and install these in the <span class="box">ubuntu Software Centre</span>. Make sure you click <span class="box">Show # Technical Items</span> (bottom-left).

## Customizing

Open <span class="box">Grub Customizer</span>. You will have to enter your password. When you are asked: <span class="box">BURG found! Do you want to configure BURG instead of grub2?</span>, click <span class="box">Yes</span>.

Click <span class="box">Install to MBR</span> (under File) to put Burg down as the default (over grub). Accept the default value unless you are booting from a hard drive other than the first one. If you're unsure, leave it as it is.

I usually untick Ubuntu (recovery mode) because it's not something i want in my normal boot. This leaves me with Ubuntu 12.04 and Windows 7 (yours might be different). Under <span class="box">Preferences</span> you can also set the timeout and default boot item. Click the <span class="box">Save</span> button when you're happy, and close it.
  
Next, we're going to change the theme (the default isn't up to much). Open the Terminal and execute the following:

```bash
sudo burg-emu
```

Provide your password and a screen like this should appear:

[![burg-emu Output]({{ '/assets/images/how-to/make-your-dual-boot-better-with-burg/burg-emu.png' | relative_url }})]({{ '/assets/images/how-to/make-your-dual-boot-better-with-burg/burg-emu.png' | relative_url }})

Press <span class="box">F2</span> and use the arrow keys to change the selected theme. I use radiance (looks like ubuntu, the one in the screenshot). Close the windows once you have made your selection (it saves automatically). The next time you start your computer, you will be able to choose your operating system in style.

## Congratulations, you have just made your Dual Boot better with Burg!
