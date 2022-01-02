---
title: How to Install and Update avast! Antivirus in Ubuntu
breadcrumb: avast! antivirus
excerpt: Ubuntu doesn't tend to get viruses, but if you work with Windows, you can scan your machine using avast! Antivirus, once you've fixed the update issue.
---

Ubuntu doesn't tend to get viruses, but if you work with Windows, you can scan your machine using avast! Antivirus, once you've fixed the update issue.

## 1. Download avast! Linux Home Edition

If you are using Ubuntu, you should download the deb version.

[.Deb Download (27.7 MB)](http://files.avast.com/files/linux/avast4workstation_1.3.0-2_i386.deb){:.btn.download}
[Alternative .Deb Download (27.7 MB)](https://linux.softpedia.com/get/Security/avast-Linux-Home-Edition-43586.shtml#download){:.btn.download.archive}

## 2. Install avast! Linux Home Edition

Once you have downloaded the package, you should have a file called <span class="box">avast4workstation_..._i386.deb</span>. It should be around 30 Megabytes. Double-Click to open it in the <span class="box">Ubuntu Software Centre</span>. Click the <span class="box">Install</span> button in the top-right-hand corner. Wait for it to finish installing before proceeding.

[![Install avast! Free Antivirus Linux Home Edition with the Ubuntu Software Centre]({{ '/assets/images/how-to/install-and-update-avast-antivirus-in-ubuntu/Screenshot-from-2012-07-22-195517.png' | relative_url }})]({{ '/assets/images/how-to/install-and-update-avast-antivirus-in-ubuntu/Screenshot-from-2012-07-22-195517.png' | relative_url }})

You will need to complete the <a href="http://www.avast.com/registration-free-antivirus.php">Registration Form</a> to receive your free Key (via email) to use avast! Antivirus for Linux.

The form asks your name, email, and country (all compulsory). Optional items include age, computer literacy, and previous antivirus, and your reason for choosing avast!. After entering your details, it states a license key will be emailed to you, usually within half-an-hour.

### Important Notes

- I have registered several installations with the same key, with no repercussions so far.
- While a valid email is required (it's where your key's being sent), I have never received any other mail from them.

When you launch avast! you will be asked for a key. If you exit without entering one, it will ask again on next launch. Because of the random nature of the key, you should copy and paste it from your registration email instead of typing it manually.

## 4. Fix the Update System

Unfortunately, while most of avast! works straight out of the metaphorical box, there is one problem.

The updates for avast! (important for detecting the latest viruses) come in blocks. <strong>Big blocks.</strong> Too big for Ubuntu's default <span class="box">shmmax<span>.

ShmMax is the maximum amount of shared memory any given process can have, and while it's probably not big enough for pretty much everything, single big temporary downloads (like those for applying big updates) means avast! usually wants more, and exits with an Update Engine Error.
  
To fix it, we need to edit a file manually, which can be done in <span class="box">Gedit</span> via the <span class="box">Terminal</span>.
  
```bash
gksudo gedit /etc/init.d/rcS
```

Add this line of code in a new line directly **before** the line, which should already be there, <span class="box">exec /etc/init.d/rc S</span>.

```bash
sysctl -w kernel.shmmax=128000000
```

Because you've edited the Kernel settings, which are things that load very early on, you'll need to restart your computer before completing the next step.

## 5. Update avast! Linux Home Edition

Updating is ridiculously easy, there is a big <span class="box">Update Database</span> button in the top-left-hand corner, and you can also go via <span class="box">Tools</span>, <span class="box">Update Database</span>.

Under <span class="box">Tools</span>, <span class="box">Preferences</span>, you can also set it to install updates automatically.

## Congratulations, you have just Installed and Updated avast! Antivirus in Ubuntu!
