---
layout: post
title:      "Gosu Ruby Gem and WSL"
date:       2021-12-05 23:53:41 +0000
permalink:  gosu_ruby_gem_and_wsl
---


[Gosu](https://www.libgosu.org/ruby.html) is a popular 2D game development library for Ruby (also available for C++). Gosu has support for Windows, Mac OS, and Linux. This would lead one to believe that it will be compatible with the Windows Substyem for Linux, or [WSL](https://docs.microsoft.com/en-us/windows/wsl/about). If you are unfamiliar with WSL, I would suggest reading the previous link, but at a high level it enables the use of a GNU/Linux environment directly within Windows itself. However, after installing the Gosu gem, and setting up a basic project that would create the game window, users will run into error(s) including:

```
error: XDG_RUNTIME_DIR not set in the environment.
Error: (SDL_Init) No available video device
error: XDG_RUNTIME_DIR not set in the environment.
Error: (SDL_CreateWindow) No available video device
Error: (GL2 / SDL_GL_CreateContext) Video subsystem has not been initialized
Error: An OpenGL context could not be created
```

What do all of these errors mean? In short, the WSL environment does not have access to your devices' display adapter, and as such can not actually render any graphics, including your newly coded game window! This would seemingly be the end of the line for Gosu and WSL support. However, to the rescue comes WSL 2, and it's later update WSLg. 

First, let's talk about WSL 2. Released as part of the Windows 10 version 2004 update on May 27th 2020, WSL 2 implemented several upgrades over the original WSL 1. A full comparison can be seen [here](https://docs.microsoft.com/en-us/windows/wsl/compare-versions). Take note of the "full system call compatibility" feature now available in WSL 2. What does this mean? Because WSL 2 now includes its own full Linux kernel, it has the ability to make system calls, which perform functions such as accessing files, creating processes, and *requesting memory*. That last one is the key here.

While WSL 2 did not launch initially with the ability to request memory from your devices' display adapter (or GPU), it was later added as part of the WSLg (or Windows Subsytem for Linux GUI) update which was announced in May of 2021 at Microsoft Build 2021. While it was initially only a feature for [Windows 10 insider](https://insider.windows.com/en-us/) (essentially preview features not yet availble to the public at large) builds, with the release of Windows 11 on October 5th 2021, WSLg began being included in production Windows builds. 

With these recent releases, Gosu (as well as any other GUI dependent libraries) can now be used with the WSL. If you are currently using WSL and are interested in trying Gosu or any other library that was previously not supported, check out:

[How to upgrade to Windows 11 now](https://www.howtogeek.com/767274/how-to-force-the-windows-11-update-and-upgrade-immediately/)
and
[Upgrading from WSL 1 to WSL 2](https://www.tenforums.com/tutorials/164301-how-update-wsl-wsl-2-windows-10-a.html) (note: while this guide says for Windows 10, it is fully compatible with Windows 11 as well, and can be done either before or after upgrading your Windows version).
