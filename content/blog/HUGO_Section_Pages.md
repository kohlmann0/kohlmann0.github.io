---
title: "Michael Kohlmann"
date: 2018-01-27T17:21:42-06:00
draft: True
---


Place holder -- 
So this is really dumb, but it looks like the file structure for making section pages (ie. the base page for the "blog" or base page for "services") does not go exactly as you would expect.

Where the homepage goes in ~/layouts/index.html

The sections go under the _defaults folder, instead of the "section" folder like I would expect. 
So instead of it being:
~/layouts/blog/index.html like the main page

it really ends up being:
~/layouts/_defaults/blog.html --> ~/blog/index.html
~/layouts/_defaults/services.html --> ~/service/index.html

<!--more-->
