---
title: How to Remove the Rhythmbox Sound Indicator from Ubuntu
breadcrumb: remove rhythmbox sound indicator
excerpt: While some may find it useful to have music players listed in the sound indicator menu with individual controls, installers of multiple software may want to blacklist some media players from appearing there. It can be done with this simple command, or edited in dconf Editor.
---

While some may find it useful to have music players listed in the sound indicator menu with individual controls, installers of multiple software may want to blacklist some media players from appearing there. It can be done with this simple command, or edited in dconf Editor.

First, open the Terminal. Then execute the following code:

```bash
gsettings set com.canonical.indicator.sound blacklisted-media-players "['rhythmbox']"
```

## Congratulations, you have just Removed the Rhythmbox Sound Indicator in Ubuntu!
