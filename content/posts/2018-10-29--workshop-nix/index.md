---
title: Workshop on Linux and Unix, Fall 2018, NSU
category: "python"
cover: tux-1531289_960_720.png
author: Shawon Ashraf
---
## Notes before coming to the workshop
-  Bring your laptop and make sure it's fully charged! 
-  Download the `Ubuntu 18.04 Image` __(32 bit if you're already using 32 bit OS, 64 bit otherwise)__
-  Download and install `Oracle VirtualBox`. You can find the download link [here](https://www.virtualbox.org)
-  If you own a `MacBook/MacBook Pro/MacBook Air`, you can skip installing `Ubuntu`, you can follow along without that as well. However, there's no problem if you install `Ubuntu` on VirtualBox.
-  Keep a fresh mind. There'll be a lot of theoretical stuff to bore you up. If drinking water makes you feel better in such situations, feel free to do so 🤓
-  Mac users - please make sure to have [Atom](https://atom.io) / [VSCode](https://code.visualstudio.com) installed to make writing some stuff in an easier way.
-  Don't be shy to ask questions. I may not know everything but I'll try to answer your questions as best as I can.

## Installing Ubuntu on VirtualBox on Windows
__Because it's pretty straightforward on macOS, ahem!__

## Step - 1 : Check if your CPU supports Virtualization
If your CPU doesn't support `virtualization` you won't be able to run VirtualBox.

So to check that, open `Task Manager`, then go to `Performance` tab, and check if `virtualization` is enabled or not. If it's disabled, than go to BIOS of your computer and enable `Intel Virtualization Technology`, `Intel VT-d` or just `Virtualization` - whatever your computer supports. Then come back to `Task Manager` and check again. It it's enabled, you're good to go.

![Imgur](https://i.imgur.com/GkDF5Ib.png)

## Step - 2 : Now open up VirtualBox

It should look like this -

![Imgur](https://i.imgur.com/pxj20UE.png)

Now, for some people, even after turning on Virtualization, the option to install __64 bit OS__ won't show up. That's because you've Hyper-V enabled on Windows and you've to disable that. Follow [this guide to disable hyper-v](http://www.fixedbyvonnie.com/2014/11/virtualbox-showing-32-bit-guest-versions-64-bit-host-os/)

Now go on and give your `Virtual Machine` a name. For example, I've named it as `UbuntuVM`.

## Step - 3 : Configure VM

Now you need to configure `RAM`, create `Virtual Hard Drives` and etc. Follow along as the images go.

Ram                       |   Virtual HDD Size             |
:-----------------------: | :----------------------------: |
![Imgur](https://i.imgur.com/FnIi5zu.png) | ![Imgur](https://i.imgur.com/L3ZFqsx.png) |


Virtual HDD                     |   Select VMDK            | Dynamic Allocation |
:-----------------------: | :----------------------------: | :------------------:|
![Imgur](https://i.imgur.com/IJfYjue.png) | ![Imgur](https://i.imgur.com/j6Pw79A.png) | ![Imgur](https://i.imgur.com/7Lm5Qrt.png) |

## Step - 4 : Start Your Virtual Machine

When you start the `Virtual Machine`, VirtualBox will ask for the boot image, which is your `Ubuntu Installation image`. Point to that using the folder icon on the prompt and then click on Start.

![Imgur](https://i.imgur.com/53N2Yuu.png)

## Step - 5 : Install Ubuntu

When Ubuntu starts up it'll ask you whether you want to install Ubuntu or just try it out. Click on `Install Ubuntu`.

![Imgur](https://i.imgur.com/QZ7yjBN.png)

Now just go on and select your keyboard layout and installation options as shown.

Keyboard                      |   Installation              |
:-----------------------: | :----------------------------: |
![Imgur](https://i.imgur.com/luThXeL.png) | ![Imgur](https://i.imgur.com/4WGTB6q.png)

Now for the tricky part. You need to partition the `Virtual Hard Drive`. You can just go on and click on Erase and use all the disk space but let's get to know how partitioning works here. 

Create a new partitoning tabel, then, create two partions, one with 500MB and `/boot` mount point and another with the rest of the space and `/` mount point. (just recall what you saw in the workshop).

![Imgur](https://i.imgur.com/o52xV0d.png)

Now just go on and click on "Install Now" and the rest of the process is just Continue Yes No stuff. And yes, don't forget about this one!

![Imgur](https://i.imgur.com/u5gFPcL.png)

## Step - 6 : Wait for the installation to finish

![Imgur](https://i.imgur.com/Sk2Gazt.png)

## Step - 7 : Done!
You're done installing, now go on and start using Ubuntu!
