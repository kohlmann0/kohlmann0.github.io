---
title: "Chocolatey -- An Introduction"
date: 2018-06-28
draft: false
---

### Chocolatey ###

What is it, what does it do, and how can it help me as a developer?

<!--more-->

Chocolatey, despite its candy coated name, is one of the first package managers I've seen for the Windows environment, that actually has some packages I like. If you are familiar with Linux, python, or Node.JS, you've probably used a package manager before, with commands like...

* apt-get for Linux
* pip for python
* npm for node.js

For Windows, there hasn't really been much similar. One might argue that the windows store might be considered one, but it's not exactly the same.

### I've never used a package manager, what does it do? ###

The short answer is that it's an easy way for you to find and install a variety of different programs. So easy, you can write a script to repeatably rebuild a brand new machine from scratch! The big difference between it, and the Windows store is that it is decentralized, and maintained by users rather than a single company. In most cases you can run a simple command line string to find, download, install, and configure a program. Chocolately handles all the files and installation. You can also use it to update or uninstall a program already installed by Chocolatey.

#### Okay, but how does that help me? ####

Well, for one thing, it's got some great software in it. Things like Visual Studio code, Chrome and Firefox, Git, Node.Js. I just used it to rebuild the machine I am working on right now. Pretty much anything people want to make available, and it's constantly growing.

Secondly, picture this. Because it's all command line, imagine running a script to install and configure an entire new machine. Or 20 new employee machines. Everything I listed above, plus an email client, Slack, VNC player, Putty, Curl, the whole works, from one Power Shell script. Your IT guys needs to spin up 20 new identical development boxes? Chocolatey. Need to install some software on a server from a remote command line? Perfect. Picked up a nasty virus, and need to reinstall Windows from scratch, Chocolatey can get you back up and running fast when you're done.

#### Awesome, I'm convinced! Let me at it! ####

Here is a quick one-liner to install it. From your command line run:

<code>@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"</code>

Or From BASH:

<code>Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))</code>

Your mileage may vary, but here are some of my favorites software installs:

* [Visual Studio Code](https://chocolatey.org/packages/vscode "Visual Studio Code Editor") (choco install vscode)
* [GIT command line tool](https://chocolatey.org/packages/git "GIT Source Control Software") (choco install git)
* [GitHub Desktop](https://chocolatey.org/packages/GitHub "GitHub Graphic User Interface App") (choco install github)
* [Google Chrome](https://chocolatey.org/packages/GoogleChrome "Google Chrome Browser") (choco install googlechrome)
* [Firefox](https://chocolatey.org/packages/Firefox "Mozilla's Firefox Browser") (choco install firefox)
* [Node.JS](https://chocolatey.org/packages/nodejs.install "The Node JS engine") (choco install nodejs.install)

There are many more. You can check out their library of packages [here](https://chocolatey.org/packages "Chololatey Package Library")



