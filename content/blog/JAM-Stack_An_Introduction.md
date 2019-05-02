---
title: "JAM Stack -- An Introduction"
date: 2018-07-30
draft: false
---

# What is the JAM Stack #

First - What the heck are we even talking about?! If you are relatively new to hosting a website yourself, when we refer to the "Stack", we mean how is it hosted and what technologies are being used. It's not always an exact one-to-one between stacks.

<!--more-->
__J.A.M.__

*   __J__ - JavaScript
*   __A__ - API's
*   __M__ - Markdown or Markup

For comparison, another popular stack, the __LAMP__ consists of 

* __L__inux OS 
* __A__pache http server  
* __M__ySQL database 
* __P__HP backend server logic. 


Or, alternatively a __MEAN__ stack is 

* __M__ongoDB 
* __E__xpressJS 
* __A__ngularJS
* __N__odeJS. 

The differences between the JAM and the other two have to do mostly with when the HTML content is created.

Unlike LAMP or MEAN, the JAM stack tries to do away with server-side rendering. Instead you could almost say, JAM stack goes "old-school," trying to do everything it can with pre-generated HTML web pages, CSS and Javascript. 

Think of it like this:

* Server Side Rendering: When the client (ie. web browser) makes a call to the server, the server takes in a set of parameters (like a name, or product ID), and creates a custom HTML file based off those parameters, on-the-fly, and returns it to client. This takes some non-zero amount of processing to render the final product.

* Jam Stack (Compile-time rendering): Instead of having a dynamic page created for each call, the HTML is created in advance at compile time, and then uploaded as a flat HTML file. When the client calls the webserver, it doesn't have to any extra processing, it doesn't have to lookup any data-base information, it doesn't have to hit another server to get additional information. It is all done once, in advance, and the webserver just has to return the finished file to the client.

But don't let that flat HTML file make you think you can't have dynamic content. You still have Javascript and Web Assembly, and all the goodies that gives you. Think of a flat HTML file, with a little sprinkling of "PWA" or "SPA" to finish off any dynamic information you need (like your current number of widgets in stock, or the current time and temperature).

The time from the initial call to the first page render is blazing fast, making your site seem fast and responsive. It's great for things "Above the Fold", and then you can lazy load the remaining data as needed. 

A "general rule of thumb" is, JAM stack is great for things that rarely change, like product descriptions, menu's, contact information, etc. It's weaker, but still very usable, for anything that changes constantly.

It gets even faster when you can upload your files to a Content Delivery Network (CDN) like Netlify or Cloud-Flare for global, redundant, localized, distribution. You can even cache the pages for a great off-line experience.

### API's ###

One thing to note is that it is a little bit of a cheat to say that there is no server side code, because the API backend that the javascript calls is obviously server side code. 

Just for an exmaple, you can hook into some great API's like Google Maps, Google Analytics, Facebook, Twitter, Amazon, SoundCloud, etc. Or, ones that you create yourself.

The big difference here is when and where the HTML webpage is rendered. JAM stack pages can be either hand-coded HTML pages or pre-compiled HTML templates (more on this later), but the end result is static file that sits on a webserver just like any other file. The request and turn around is about as fast as you can possibly be, to get content on the screen. Other stacks will sometimes take the request, hit the database for information, process it, generate the text of a webpage... all that before even sending the first byte back to the client.


### Here's an example ###
This site itself is considered a JAM Stack. I use a "Static Site Generator" called Hugo. Jekyll is another popular example for linux and Mac, built on Ruby.

* I created several template files to create a common layout.
* I then use markdown to write the actual content, quicker than I could in raw HTML. 
* Then Hugo takes the template and content and compiles it into individual HTML, JavaScript and CSS files. 
* Then I commit it to Github which serves up the files for free at kohlmann0.github.io. 

One advantage to this is, because public Github repositories are free, and because Netlify.com will give you a custom domain name for free, this is all completely free, expandable, and still dynamic through JavaScript to make it seem like any other site.

I'd like to talk a bit more about Hugo, Javascript and tips and tricks to give it some dynamic content, so stay tuned for later posts, which I will eventually link below.

### One Final Word ###

Think about the content of your current website. How much does your content change. What parts remain constant, and what parts need constant updating. Specifically the "old stuff". Adding new stuff to a blog or product item to a store for examples is the same amount of time, whether you use Wordpress or JAM-stack. But once you have that content out there... How often do you actually go back and rewrite that blog post? Does the description of the product change very often? Are you changing your pricing every day? How often would you actually need to rebuild a single page on your site, that can't be done through an API call or lookup?

I think you owe it to yourself to investigate how you can speed up and improve your own site. And besides... Nothing says you can't leverage both server-side, and compile time rendering.


## Some useful links ##

* [Jamstack.Org](https://jamstack.org) - full of useful resource, best practices, and examples.
* [Static Site Generators](https://www.staticgen.com/)

Source Control Solutions

* [Github](https://github.com)
* [GitLab](https://gitlab.com/)
* [BitBucket](https://bitbucket.org/)

Content Delivery Networks (hosting)

* [Netlify](http://www.netlify.com)
* [Cloudflare](https://www.cloudflare.com/)