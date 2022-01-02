---
title: How to Install or Upgrade to the latest version of GIMP in Ubuntu
breadcrumb: install or upgrade to the latest version of gimp
excerpt: GIMP is one of the most popular image editing programs that doesn't cost big money. This free programme is frequently tooted as an alternative for Adobe Photoshop. Unfortunately, the Ubuntu sources don't tend to stock the most recent version.
---

Gimp is one of the most popular image editing programs that doesn't cost big money. This free programme is frequently tooted as an alternative for Adobe Photoshop. Unfortunately, the Ubuntu sources don't tend to stock the most recent version.

Adding the repository, updating, and installing the latest gimp, can be done via the command line. Copy commands one line at a time and execute them individually.

The first command adds a new repository to use as a software source. It will ask for an administrator (root) password, and check for updates.

The second command installs Gimp, or updates it if it is already installed. It will also install or update any dependencies (required packages/software).

```bash
sudo add-apt-repository ppa:otto-kesselgulasch/gimp
sudo apt install gimp
```

## Congratulations, you have just Installed or Upgraded Gimp in Ubuntu!
