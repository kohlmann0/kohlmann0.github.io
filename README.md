# Michael Kohlmann
[![Netlify Status](https://api.netlify.com/api/v1/badges/33ac6b0f-8553-47ba-a203-a333310fd39a/deploy-status)](https://app.netlify.com/sites/elegant-swartz-0fef87/deploys)


This is an experiment in building and hosting an ultra-cheap website. The goal is to get it as close to free as possible, while using a solid development tool chain. I'll try keep this readme up to date with the latest tooling details.



## Current Technologies and Tool Chains

Hosting Stack: JAM Stack

- Using github.com to host static pages, built with a static site generator.

- Netlify.com to provide a astatic IP address

- [Todo] LetsEncrypt to provide https encryption certificate



Static page/site Generation:

- HUGO



Editing Device:

- I setup the initial Hugo site and template on a Windows 10 machine, just because it was faster it iterate through the layout changes I wanted.

- However, the end goal is to be able to use iPad while I'm on the road for convenience...



Source Control:

- Git on Github.com

- Windows 10 - Git command line or Git Desktop typically. larger projects, I tend to use the TFS git integration 

- [Todo] iPad - Working Copy app



Build pipeline

- Windows 10 - HUGO site builder

- Github - Source Control checkin

- Netlify monitors Github, and kicks of a continuous integration build and host



Editor/IDE:

- Windows 10 - Visual Studio Code (but could easily be done with Notepad++ or Sublime)

- [Todo] iPad - Working Copy has a built in editor.
