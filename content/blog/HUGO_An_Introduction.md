---
title: "HUGO_An_Introduction"
date: 2019-04-22T14:08:00-05:00
draft: false
---

### Hugo - An Introduction ###

What is Hugo?

If you've read some of my other posts, you may already know that Hugo is a "Static Site Generator". 

A static site generator takes a bunch of modular HTML/Javascript/CSS "components" and forms a single HTML file out of the reusable pieces.

If you are familiar with any of the modern technology stacks like ASP.Net, React, Ruby, etc. you are probably familiar with using small, reusable, modular pieces to create a whole webpage. Think of a static site generator as something similar, except that instead of dynamically creating the HTML at run-time, it pre-compiles it at build time, and placed on a server as a complete HTML file. See my blog about [JAM Stacks]() for a few more details about why this is awesome.

### Static Site Generator Advantages ###

There are quite a few advantages to this. For starters, serving up individual HTML files is way faster than assembling it on-the-fly each time.

Secondly, because it is a static file, it tends to get a better search engine optimization (SEO) score (for various reasons which I am still looking into myself.)

Additionally reuse of code become much easier. For example, write the code for Navigation bar once, and reuse it on every page with a single tag. In the "good-old-days", at the start of the world wide web, you had to rewrite it for each page. God forbid you ever needed to change it.

### Hugo advantages ###

Of the hundreds site generators out there, why use Hugo?

At this point, what makes Hugo better than everyone else, is really just a matter of opinion. Not going to lie there, a lot of them are pretty similar. 

What Hugo does to well though, is:

* Extremely quick build time, and even a "live build". Everytime you save your file, it will update with your changes.
* Good community support (at least better than most of the others)
* 3rd party tutorials on YouTube, and a fairly large user-base.

### Hugo disadvantages ###

It's hard to come up with any real disadvantages to Hugo. Personal preferences yes. Their formal documentation is a bit atrocious compared to Microsoft's or Mozilla's documentation, but I've certainly seen worse. Google is better help than scrolling though their docs. Being used to Javascript or C# or really any other formal language, I'm not really a fan of their logic syntax.

This is perfect for inserting variable....

~~~
<title>{{ .Title }}</title>
~~~

It's clear, concise, makes sense, straight forward for the most part. I wish it was all that clear.

This if statement, with the Or at the start, and "space" separated arguments threw me at first.

~~~
{{ if or (isset .Params "alt") (isset .Params "caption") }} Caption {{ end }}
~~~

This one, I couldn't for the life of me, figure out how to pass your data from one partial to another.

~~~
{{ partialCached "header.html" . }}
or
{{ partialCached "footer.html" . .Section }}
~~~

You see that period there? That single little period, all by itself, that is so easy to skip over and not notice? That is the most important part. Somehow a period represents your base data object in Hugo. No where have I found that explained. I only got there through following code samples and trial-and-error.

Other than that minor pet-peeve about how to pass around data, and the general format of their logic, I really can't complain. You get used to it pretty quick, and you really only have to set it up the first time. After you have something you like, in theory, it's just adding more content, and maybe some minor tweaking.


So, that's my 'not-so-quick' introduction to HUGO. Really, I think Static sites are the way to go in most situations. Very light weight, SEO loves it, and can be as flexible as you want it to be.

