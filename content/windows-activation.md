---
title: "Install Activated Windows for Free, legally"
date: 2024-01-14T20:43:46Z
draft: false
tags: ["Life Hacks"]
---

# Introduction

The day may unfortunately come when you are required to use the Windows operating system, usually for work obligations. Not only are you forced to use Windows, but Microsoft also tries to pressure you into paying for the "privilege" of using their operating system. At the time of writing, Windows 11 Home edition is currently being sold for £120.00! There are also many third-party sellers selling Windows Activation Keys for a cheaper price, although a lot of them are scams/unreliable. What most people don't realise is that you can download, install, and activate Windows without ever paying a penny.

# Download

This guide is designed to work for people on Linux distros. Microsoft has a much easier process to download Windows if you already have access to a Windows machine, but this guide works for everyone. You first need to download the Windows Disk Image ISO from [here](https://www.microsoft.com/software-download/windows11) on the Microsoft website. This download is very slow from Microsoft, regardless of how quick your internet speeds are, but unfortunately you'll have to wait it out. It took ~2 hours for me to complete. Downloading from a torrent may be much quicker, but I wouldn't trust any public torrent for things like this.

You then need to flash this ISO onto a USB stick. The particular disk formatting/labelling and partitions that Windows requires is frustratingly precise and very delicate (unlike installing Linux operating systems). Thus I would recommend using a third-party tool like [WoeUSB](https://github.com/WoeUSB/WoeUSB) to do the work for you. You simply specify the ISO file, your USB stick's partition, and let it do its thing. With [WoeUSB](https://github.com/WoeUSB/WoeUSB), I'd recommend ticking the skip legacy grub bootloader flag to save time. Note that whatever method you use, this flashing process also takes up a lot of time depending on the write speed of your USB stick. You should also ensure that you do not remove your USB stick until you have ran the `sync` command.

# Installation

Once you have flashed Windows onto your USB stick, you can insert it into your computer and then on startup, it will either automatically boot from the USB stick, or you will manually have to interrupt the boot process by spamming F12, Enter, Esc, or some other key and specify that you want to boot from the USB stick. At some stage after hitting "Next" a few times, Windows will prompt you to enter in a License Key. What most people don't realise is that you can simply click on "I do not have a License Key", and the installation process will continue exactly as normal. No purchase required.

The problem however is that your Windows will be "unactivated". This has very little effect for most people, beyond just the fact that you won't be able to change your background wallpaper, and there'll be an ugly activation message in the bottom right hand corner of your Desktop. Luckily, you can also activate your Windows for free and very easily.

# Activation

Luckily, Microsoft leaves behind a lot of backdoors for Microsoft technicians and their various services to be able to activate Windows even without a valid product key. But any of us can also use those same backdoors. I recommend the program found at [massgrave.dev](https://massgrave.dev/) to do this for you. If you follow the instructions on that website, which involve basically just running one command in your terminal, you'll end up with a completely activated Windows installation. It's completely indistinguishable from what most people would have to pay £120 for.
