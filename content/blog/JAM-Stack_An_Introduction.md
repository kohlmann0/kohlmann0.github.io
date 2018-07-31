---
title: "JAM Stack_An_Introduction"
date: 2018-07-30
draft: false
---

# The JAM Stack #

What is the Jam Stack, and how does it differ from other technology stacks like "LAMP" or "MEAN"?


## First - What the heck are we even talking about?! ##
For starters, if you are relatively new to hosting a website yourself, when I refer to the "Stack" I mean how it is hosted and the technologies used in coding it.

*   __J__ - JavaScript
*   __A__ - API's
*   __M__ - Markdown or Markup

For comparison, to another popular stack, when people refer to a __LAMP__ stack, they mean the technologies of 

* __L__inux OS 
* __A__pache http server  
* __M__ySQL database 
* __P__HP backend server logic. 

<!--more-->

Or, alternatively a __MEAN__ stack is 

* __M__ongoDB 
* __E__xpressJS 
* __A__ngularJS
* __N__odeJS. 

How did it get the name JAM Stack? There isn't an exact definition to how these stacks get named, it's usually just a set of letters to form a catchy phrase.

Unlike technology stacks that do server side rendering (like asp.net, PHP, Java, that have code to generate webpage content on the fly), the Jam Stack is all static HTML, CSS, and Javascript files, served up as soon as they are requested, without any additional processing on the server. If there is any dynamic content it's done with JavaScript making API calls to get additional content in a second round-trip call. 

But don't let that second round trip worry you. The time fron the initial call to the first page render is super fast, making your site seem fast and responsive. It's great for things "Above the Fold", and then you can lazy load the remaining data as needed. It's also great for things that rarely change, like product and service descriptions, menu's, contact information, etc. It's weak for anything personalized to a specific user, like shopping cart data, or user profiles (at least on first load). It can sometimes make it a little easier to cache pages for a great off-line experience as well.

### API's ###
One thing to note is that it is a little bit of a cheat to say that there is no server side code, because the API backend that the javascript calls is obviously server side code. 

Just for an exmaple, you can hook into some great API's like Google Maps, Google Analytics, Facebook, Twitter, Amazon, SoundCloud, etc. Or, ones that you create yourself.

The big difference here is when and where the HTML webpage is rendered. JAM stack pages can be either hand-coded HTML pages or pre-compiled HTML templates (more on this later), but the end result is static file that sits on a webserver just like any other file. The request and turn around is about as fast as you can possibly be, to get content on the screen. Other stacks will sometimes take the request, hit the database for information, process it, generate the text of a webpage... all that before even sending the first byte back to the client.


### Here's an example ###
This site itself is considered a JAM Stack. I use a "Static Site Generator" called Hugo. Jekyll is another popular example for linux and Mac, built on Ruby.

* I created several template files (partials or modules) to create a common layout.
* I then use markdown to write the actual content, quicker than I could in raw HTML. 
* Then Hugo takes the template and content and compiles it into individual HTML, JavaScript and CSS files. 
* Then I commit it to Github which serves up the files for free at kohlmann0.github.io. 

One advantage to this, is because public Github repositories are free, and because Netlify.com will give you a custom domain name for free, this is all completely free, expandable, and still dynamic through JavaScript to make it seem like any other site.

I'd like to talk a bit more about Hugo, Javascript and tips and tricks to give it some dynamic content, so stay tuned for later posts, which I will eventually link below.

## Some useful links ##

* [Jamstack.Org](http://jamstack.org) - full of useful resource, best practices, and examples.
* [Static Site Generators](http://www.staticgen.com/)
* [Github](http://www.github.com) - for hosting your source code.
* [Netlify](http://www.netlify.com) - for providing you with a free domain name, and linking it to your github account.
* [Travis CI](http://www.Travis-ci.org) or something similar... this one is a give or take. You don't really need it, but it can be useful. You really only need it if you need a special step to build your code when your not on your main build machine.