---
title: How to Enable Sharing in Miro on Ubuntu
breadcrumb: enable sharing in miro
excerpt: If you have just installed Miro in Ubuntu, you may be wondering why trying to enable sharing results in an error message about the Avahi mDNSResponder Compatibility Library.
---

If you have just installed Miro in Ubuntu, you may be wondering why trying to enable sharing results in an error message about the Avahi mDNSResponder Compatibility Library. There are two ways to do this. The first column you just click the button and click install, and the second one requires the execution of a command in the terminal, but may well be faster.

## The Easy Way

All you need to do is install the Avahi mDNSResponder Compatibility Library, and then restart. No, most things in Ubuntu do _not_ require a full restart, but this one usually does. Installation can be done in two clicks, one on the link below, and then clicking the install button in the Ubuntu Software Center.

[Install Avahi mDNSResponder Compatibility Library &rsaquo;](apt:libavahi-compat-libdnssd1){:.btn.download}

After restarting, you can launch Miro and enable sharing, no more Install Avahi mDNSResponder Compatibility Library error message.
      
## In the Terminal

If you are a little more technologically adept, you may prefer to run a terminal command. Here it is:

    sudo apt-get install libavahi-compat-libdnssd1

After restarting, you can launch Miro and enable sharing, no more Install Avahi mDNSResponder Compatibility Library error message.

## Congratulations, you have just Enabled Sharing in Miro on Ubuntu!</h3>
