---
layout: post
title: "Let's start a RIOT"
date: 2018-12-09
---

Some time ago I stumbled upon a very interesting project - [RIOT OS](https://github.com/RIOT-OS/RIOT). 
There are few comprehensive guides to start using it [<sup>1</sup>](https://doc.riot-os.org/index.html#the-quickest-start) and [<sup>2</sup>](https://github.com/RIOT-OS/Tutorials/blob/master/README.md). But I have a problem with the first one: I use Mac, and it is not possible to create tap interface on macOS (or at least I couldn't do that). The second one works perfectly, but I like to configure everything by myself. 

So I've installed Arch Linux in VirtualBox (mainly because of [this](https://github.com/RIOT-OS/RIOT/wiki/Family:-native#host-systems)) and tried to follow steps mentioned in [<sup>1</sup>](https://doc.riot-os.org/index.html#the-quickest-start). At first, it didn't compile because some packages were missing (unzip and python3). Then it failed at link stage. As it turns out, as I've installed a 64-bit version of Arch, I need to install additional libs to build 32-bit code. To fix this problem, you need two additional packages:
```
pacman -S lib32-glibc
pacman -S lib32-gcc-libs
```

Happy RIOTing.
