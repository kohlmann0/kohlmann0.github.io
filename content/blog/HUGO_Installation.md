---
title: "HUGO_Installation"
date: 2018-03-13T14:08:04-05:00
draft: true
---

I've gone through installing Hugo on two different machines now.

The first time went super easy. I used the [Chocolatey package manager]() to install it. One line in the windows command line and -Boom- up and running, no big deal.

The second time I decided to try the instructions for [Installing on Windows](). This one didn't go as smoothly, so I decided to write a little note about it so I could remember what I did to fix it later.

The problem I ran into was that I couldn't get the PATH to stay. When I restarted the machine, or closed the windows command line window and reopen it, it would forget it's path to the Hugo install.

What ended up working for me instead was manually adding it via the Path's UI in windows.

<!--more-->