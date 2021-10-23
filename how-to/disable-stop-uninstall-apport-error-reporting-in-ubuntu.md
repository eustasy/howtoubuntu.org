---
title: How to Disable, Stop, or Uninstall Apport Error Reporting in Ubuntu
breadcrumb: disable stop or uninstall apport error reporting
excerpt: 64-bit has been the default option for some time. You should probably use that.
---

Ubuntu 12.04 is the first release of Ubuntu that ships with Apport Error Reporting enabled by default, and as a result, you may get a large quantity of <span class="box">Internal System Error</span> popups inside Ubuntu. Similar popups may also read <span class="box">Sorry, Ubuntu 12.04 has experienced an internal error.</span> These popups are part of Apport, an internal debugger which automatically generate reports to submit for packages that crash. Many reports can't be filed or have already been filed, and as such it is usually safe to turn off.

## Information

Apport is an Error Reporting Service provided by Ubuntu to intercept and analyze crashes and bugs as and when they occur. Crashes and Bugs may sound like bad things, but actually most operating systems will have several a day, and it doesn't mean your computer is broken, nor does it necessarily stop working. As such, Apport can usually be safely disabled, as it doesn't fix anything, it just tells developers that something went wrong.

## Stop Apport (until reboot)

You can stop the currently running Apport service with the following command:

    sudo service apport stop

Note that unless you remove it or disable it at boot it will start again the next time you turn on your computer.

## Disable Apport at Boot

You need to manually edit a file to Stop Apport Running at Boot (when you turn on your machine. Open the Terminal, and paste the following command with <span class="box">Ctrl</span>+<span class="box">Shift</span>+<span class="box">V</span>, or type it in manually.

    sudo nano /etc/default/apport

Change the line that says <span class="box">enabled=1</span> to <span class="box">enabled=0</span> to disable Apport. Use <span class="box">Ctrl</span>+<span class="box">X</span> to exit and <span class="box">Enter</span> to save. To re-enable, change it back.

## Uninstall Apport

It is fairly simple to uninstall Apport, as you can open the **Ubuntu Software Centre**, search for <span class="box">apport</span>, and simply click <span class="box">Remove</span>.

A similar process can be used for the package <span class="box">apport</span> in both **Synaptic** and in **apt** the **Terminal**.

    sudo apt-get purge apport

## Congratulations, you have Disabled, Stopped, or Uninstalled Apport Error Reporting in Ubuntu!
