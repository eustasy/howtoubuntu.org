---
title: How to Install a 32-bit program in 64-bit Ubuntu
breadcrumb: install a 32-bit program in 64-bit
excerpt: Since Ubuntu 12.04 and 13.10 started recommending 64-bit for most users, you may find that some software doesn't have a 64-bit counterpart.
---

Since Ubuntu 12.04 and 13.10 started recommending 64-bit for most users, you may find that some software doesn't have a 64-bit counterpart.

If an application you need to use does not have a 64-bit version available, you can trick it into thinking you're still running 32-bit.

## Warnings

Some software may not work this way. Some may cause damage that should be easily reversible (no promises). Unfortunately, we can't help every individual case, but you can [askubuntu.com](http://askubuntu.com/) about specific pieces of software if this doesn't work.

## 1. Check for a 64-bit version

First, check to see if the package you want is available in 64-bit. Try googling around, 32-bit will have i386, i586 or i686 in the name, whereas amd64 indicates 64-bit. You might want to include amd64 in your search terms.

## 2. Trick the app

Start by installing the package <span class="box">[ia32-libs](apt:ia32-libs)</span>. Clicking that link should open the Ubuntu Software Centre, and the install button is located near the top-right-hand corner. If that doesn't work, then try searching for it in the Software Centre. You might have to click "Show # Technical Items" (bottom left).

Alternatively, you can run the following in the terminal, providing your password when prompted.

```bash
sudo apt-get install ia32-libs
```

## 3. Install

If you program will still not install (try doing it the normal way), grab a .Deb and try it manually.

```bash
sudo dpkg --force-architecture -i Downloads/download.deb
```

## Congratulations, you have just Installed a 32-bit program in 64-bit Ubuntu!
