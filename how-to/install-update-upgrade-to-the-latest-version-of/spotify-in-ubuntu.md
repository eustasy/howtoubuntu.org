---
title: How to Install Spotify in Ubuntu
breadcrumb: spotify
excerpt: While Spotify has no supported release for Linux as such, there is, hidden away a little bit, a nice little "Preview" release that runs reasonably well, even if it is not the most native of applications.
---

While Spotify has no supported release for Linux as such, there is, hidden away a little bit, a nice little "Preview" release that runs reasonably well, even if it is not the most native of applications.

> This is a preview build of Spotify for Linux. As a preview release this version is still unsupported, but we're running it ourselves and will try to make sure it keeps pace with its Mac and Windows siblings.
- [Spotify](https://www.spotify.com/download/linux/) is a great way to listen to music by streaming it on your phone, in your browser, or on your Linux desktop. You can stream everything, upgrade and sync tracks and playlists offline, or purchase individual tracks to keep forever.

## Install from Ubuntu Store (18.04 LTS / 20.04 LTS and above)

[Install on Ubuntu Store](snap://spotify){:.btn.download}

## Install with Snap (14.04 LTS and above)

The following two lines will install the Spotify snap. Once installed, you'll get updates to the Spotify client as and when the developers upload it to the store. You should copy and paste this code into your Terminal and execute it.

```bash
sudo apt install snapd
snap install spotify
```

## Install Desktop Edition (any version)

```bash
curl -sS https://download.spotify.com/debian/pubkey_5E3C45D7B312C643.gpg | sudo apt-key add - 
echo "deb http://repository.spotify.com stable non-free" | sudo tee /etc/apt/sources.list.d/spotify.list
sudo apt update
sudo apt install spotify-client
```

You can get support for this build of Spotify on their [community support site](https://community.spotify.com/t5/Desktop-Linux/bd-p/desktop_linux).
