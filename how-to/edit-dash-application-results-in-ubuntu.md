---
title: How to Edit Dash Application Results in Ubuntu
breadcrumb: edit dash application results
excerpt: When you search for something in the Unity Dash, you may wish to remove some of the applications listed, or add some that are either hidden by default, or simply don't exist.

When you search for something in the Unity Dash, you may wish to remove some of the applications listed, or add some that are either hidden by default, or simply don't exist.

## With Alacarte

### Install Alacarte

First, you will need to install a menu editor. This is what we will be using to edit our application results. We will be using Alacarte.

[Install Alacarte &rsaquo;](apt:alacarte){:.download}

If asked, confirm that How To Ubuntu (this site) should be allowed to open the Ubuntu Software Centre. This does now allow us to install software at any time. You will **always** have to click install yourself. You may need to enter your password to install this piece of software.

The <span class="box">Install</span> button is located in the top-right corner of the Ubuntu Software Centre. Now, we must open the editor.

[![Install Alacarte]({{ '/assets/images/how-to/edit-dash-application-results/InstallAlacarte.png' | relative_url }})]({{ '/assets/images/how-to/edit-dash-application-results/InstallAlacarte.png' | relative_url }})

### Edit Application Results

[![Search Menu]({{ '/assets/images/how-to/edit-dash-application-results/SearchMenu.png' | relative_url }})]({{ '/assets/images/how-to/edit-dash-application-results/SearchMenu.png' | relative_url }})

You can open Alacarte by searching the Dash for <span class="box">Menu</span>, and Clicking <span class="box">Main Menu</span>. Now we can enable (un-hide), disable (hide), and permanently delete items and whole categories from here.

Categories can be found in the left-hand column. You can uncheck items or categories to hide them, and check to make them searchable again. This will not install or uninstall any software, however we recommend unchecking items rather than deleting them.

[![Edit Items]({{ '/assets/images/how-to/edit-dash-application-results/Edit.png' | relative_url }})]({{ '/assets/images/how-to/edit-dash-application-results/Edit.png' | relative_url }})

Here, we are enabling <span class="box">Software Sources</span>.

## Terminal for You

### Make a folder for the items

This folder will just be a nice, quiet, hidden place that the Dash already checks.

    mkdir -p ~/.local/share/applications

#### Copy the Launcher

    cp /usr/share/applications/software-properties-gtk.desktop ~/.local/share/applications/

### Add and or Remove

    gedit ~/.local/share/applications/software-properties-gtk.desktop

Here, we're using the <span class="box">Software Sources</span> launcher, as this is hidden by default, but might be useful to have visible for more direct access. Now we just need to change the <span class="box">NoDisplay</span> value from true to false.

    NoDisplay=true
    NoDisplay=false

Now you can find <span class="box">Software Sources</span> in the Dash. If it is not immediately available, try logging out and in again to refresh it. Reverse to hide an item.

## Terminal for Everyone

We're going to edit the root file for the <span class="box">Software Sources</span> launcher, as this is hidden by default, but might be useful to have visible for more direct access. Editing like this will enable (or disable) the launcher for everyone.

    gksudo gedit /usr/share/applications/software-properties-gtk.desktop

Now we just need to change the <span class="box">NoDisplay</span> value for this.

    NoDisplay=true
    NoDisplay=false

Now you can find <span class="box">Software Sources</span> in the Dash. If it is not immediatly available, try logging out and in again to refresh it. Reverse to hide an item.
	
## Congratulations, you have just Edited Dash Application Results in Ubuntu!
