---
title: How to Execute a .Run or .Bin file in Ubuntu
breadcrumb: execute a .run or .bin file
excerpt: .Run or .Bin files are probably the only file types you will ever need to mark as executable in normal use of Ubuntu. There are two ways to execute them,  either in the terminal or graphically .
---

.Run or .Bin files are probably the only file types you will ever need to mark as executable in normal use of Ubuntu. There are two ways to execute them (which usually installs something), either in the terminal, or graphically (which usually relies on the terminal somewhat as well). Whichever you choose, read the red warnings below.

## Warnings

.Run and .Bin files are fairly easy to execute or install, but can be notoriously difficult to remove. This depends on the developer. They also can be downloaded from anywhere, and made by anyone, so make sure you or other people have experience and therefore trust of the source. You should check any uninstall procedures before proceeding with these instructions.

Some .Run and .Bin files require root permissions to run, using the <span class="box">sudo</span> command. Remember that root access means the file has full access to your system and could potentially damage its stability and security.

## In the Terminal

First, open the Terminal, then mark the file as executable with the <span class="box">chmod</span> command.

```bash
chmod +x file-name.run
```

Now you can execute the file in the terminal.

```bash
./file-name.run
```

If an error message including a problem such as 'permission denied' appears, use <span class="box">sudo</span> to run it as root (admin). Be careful, <span class="box">sudo</span> allows you to make critical changes to your system. Many software installs will require <span class="box">sudo</span>.

```bash
sudo ./file-name.run
```

## In File Manager

### Before Executing

[![Allow Executing as a Program]({{ '/assets/images/how-to/execute-a-run-or-bin-file-in-ubuntu/Screenshot-from-2012-06-04-182041.png' | relative_url }})]({{ '/assets/images/how-to/execute-a-run-or-bin-file-in-ubuntu/Screenshot-from-2012-06-04-182041.png' | relative_url }})

First, move the .Run or .Bin file to your Home folder. This is just precautionary. Second, Right-click on the file and select <span class="box">Properties</span>. Under the <span class="box">Permissions</span> tab, tick the checkbox near the bottom labeled <span class="box">Allow executing file as program</span>. Click <span class="box">Apply Permissions</span>. Then Close the Properties Window.

### Executing

Double-click the .Run or .Bin file. If not action appears to be happening, right-click and select <span class="box">Run in Terminal</span>. A purple window with white text will open. This is the terminal. Do not worry if it takes a few seconds to appear, this is normal. Answer any questions using the <span class="box">Tab</span>, <span class="box">Arrow</span>, <span class="box">Space</span>, and <span class="box">Enter</span> keys.

## Congratulations, you have just Executed a .Run or .Bin file in Ubuntu!
