---
title: How to decide if you should use 32-bit or 64-bit Ubuntu
breadcrumb: decide if you should use 32-bit or 64-bit ubuntu
excerpt: 64-bit has been the default option for some time. You should probably use that.
---

## History

Ubuntu 12.04 and 12.10 were both set to be the first release to have 64-bit set as the "recommended" architecture, except neither did.

Canonical recommended 64-bit for both 13.10 and 12.04.3, unless you have 2GB of RAM or less.

Since then, 64-bit has been the default option unless using an "alternative" installation option.

## What are 32-bit and 64-bit?

32-bit and 64-bit are types of architecture, 32 works in 4 sets of 8 (the 8 being a byte), and 64 in 8 sets of 8. More bits mean that data is processed in larger chunks, resulting in greater speed and accuracy.

All computers made within the last 10 years are likely to have 64-bit capable CPUs, and most maintained applications and drivers have 64-bit versions available.

### Other Operating Systems

Windows 7 shipped 64-bit as default, and then Windows 10 and 11 too (we do not talk about Windows 8). mac OS has been 64-bit or similar for a while. Previously, Ubuntu shipped 32-bit as default, but both 12.04.3 and 13.10 ships with 64-bit as default, and 32-bit (with PAE) "for machines with less than 2GB of RAM".

### Decision Time

You can probably stick to the default download option of 64-bit, unless you're quite low on RAM. That way you'll be less likely to run into any unusual issues.

If your computer came with Windows 8 (or UEFI firmware), you should always use 64-bit.

Having read this, you might want to know [how to find out how much ram you have in Ubuntu]({{ '/how-to/find-out-how-much-ram-is-installed-in-ubuntu' | relative_url }}).
