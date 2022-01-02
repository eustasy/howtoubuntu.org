---
title: How to Install Skype Wrapper and Integrate Skype into Ubuntu
breadcrumb: skype wrapper
excerpt: If you've used Skype then you may have come across some of the patchy integration that is now Microsoft's problem. While they take their time fixing that, there is, in typical Linux fashion, a home-grown alternative. Skype Wrapper gives you tighter integration into Ubuntu and Unity via a convenient python app.
---

If you've used Skype then you may have come across some of the patchy integration that is now Microsoft's problem. While they take their time fixing that, there is, in typical Linux fashion, a home-grown alternative. Skype Wrapper gives you tighter integration into Ubuntu and Unity via a convenient python app.

_You also might want to [Install or Upgrade to the latest version of Skype]({{ '/how-to/install-update-upgrade-to-the-latest-version-of/skype-in-ubuntu' | relative_url }})_

## 1. Add the Source in the Terminal

Open the terminal, and execute the following line of code. This will add the Software Source, check it, and install the package you want, automatically confirming any changes.

```bash
sudo add-apt-repository ppa:skype-wrapper/ppa
```

## 2. Install Skype Wrapper

Now open <span class="box">Synaptic Package Manager</span> (you can [Install Synaptic Package Manager](apt:synaptic) if you don't already have it), enter for <span class="box">skype</span> in the search box (top, centre), and <span class="box">Right-Click</span> and <span class="box">Mark for Installation</span> the package <span class="box">skype-wrapper</span>.

Then, hit the <span class="box">Apply</span> button (a tick to the left of the search box). If it's not already, you may wish to check the <span class="box">Close this Window when finished.</span>. This will close the pop-up, but not Synaptic upon completion.

## 3. Using Skype Wrapper

First, open Skype however you usually do. Then, hold the <span class="box">Alt</span> key and press <span class="box">F2</span>. Type <span class="box">skype-wrapper</span> and hit enter into the resulting Unity layover. A pop-up will appear over the Skype window, tick the check-box to allow the Skype Wrapper to access Skype all the time.

## Congratulations, you have just Installed Skype Wrapper and Integrated Skype into Ubuntu!
