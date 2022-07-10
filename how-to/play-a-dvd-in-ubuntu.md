---
title: How to Play a DVD in Ubuntu
breadcrumb: install codec play dvd
excerpt: Ubuntu, by default, does not include the necessary libraries or codecs to decode DVDs. As such, it will not play commercial videos off of them. This is how to play a DVD in Ubuntu.
---

Ubuntu, by default, does not include the necessary libraries or codecs to decode DVDs. As such, it will not play commercial videos off of them. This is how to play a DVD in Ubuntu

## Install Codecs

### Using the Software Centre

You should click the links below one at a time. They will open the Software Centre to the correct package. You may need to allow your browser to open the Software Centre.

Once the Software Centre has opened, you can click install in the top-right-hand corner of the screen (you may be asked for your password), then close the Software Centre. You will need to click the links and then click install one at a time, but you do not need to wait for one to finish installing before proceeding to the next.

[![LibDVDCSS in the Ubuntu Software Centre]({{ '/assets/images/how-to/play-a-dvd-in-ubuntu/Screenshot-from-2012-06-04-173033.png' | relative_url }})]({{ '/assets/images/how-to/play-a-dvd-in-ubuntu/Screenshot-from-2012-06-04-173033.png' | relative_url }})
  
[Install LibDVDCSS &rsaquo;](apt:libdvdcss2?section=universe?section=multiverse) For recognizing DVDs in Ubuntu.
  
[Install LibDVDRead4 &rsaquo;](apt:libdvdread4?section=universe?section=multiverse) For reading DVDs in Ubuntu.
  
[Install LibDVDNav4 &rsaquo;](apt:libdvdnav4?section=universe?section=multiverse) For navigating DVDs in Ubuntu.
  
These are not included by default, because to pass them on to you, Canonical (who make Ubuntu) would have to pay a royalty, making Ubuntu non-free. For personal use however, they are free for you to install.

Note: If these links do not work, open the Software Center and install the packages `libdvdcss`, `libdvdread4`, and `libdvdnav4` by searching for them (upper-right-hand corner) and clicking install (only revealed when they're selected). Give your password when prompted.

### Using the Terminal

    echo 'deb http://download.videolan.org/pub/debian/stable/ /' | sudo tee -a /etc/apt/sources.list.d/libdvdcss.list &&
    echo 'deb-src http://download.videolan.org/pub/debian/stable/ /' | sudo tee -a /etc/apt/sources.list.d/libdvdcss.list &&
    wget -O - http://download.videolan.org/pub/debian/videolan-apt.asc | sudo apt-key add - &&
    sudo apt-get update &&
    sudo apt-get install libdvdcss2 libdvdread4 libdvdnav4 libavcodec-extra-53 libavformat-extra-53 libavutil-extra-51 libpostproc-extra-52 libswscale-extra-2 ubuntu-restricted-extras gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly libdvd-pkg
    
You will be prompted for your password. When you provide it, no dots, stars, or other characters will appear in place of the letters. This is normal. Proceed and hit enter.

You may need to confirm you want to install certain things using tab to navigate text-buttons and space to check boxes.

## Playing DVDs

### VLC Media Player

[![VLC Media Player]({{ '/assets/images/how-to/play-a-dvd-in-ubuntu/Screenshot-from-2012-06-04-173405.png' | relative_url }})]({{ '/assets/images/how-to/play-a-dvd-in-ubuntu/Screenshot-from-2012-06-04-173405.png' | relative_url }})

Open the dashboard and launch VLC Media Player. You can find it by searching for VLC. 

If VLC is not installed, you can [Install VLC &rsaquo;](apt:vlc)

Open VLC. If VLC does not play your DVD automatically, click **File** and select **Open Disc**.

Click **Play**.

### Totem Media Player

Open the dashboard and launch Movie Player. You can find it by searching for Totem.

If Totem does not play your DVD automatically, click **Movie** and select **Open**. Select your DVD (in the left hand column and click **Play**.
 
## Congratulations, you can now Play a DVD in Ubuntu!
