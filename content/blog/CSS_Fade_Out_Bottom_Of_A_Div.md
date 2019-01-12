---
title: "CSS Tricks - Fade out the bottom of a div (Preview)"
date: 2018-03-13T14:08:04-05:00
draft: true
---

This blog ends up being half teaching, half bookmark for little tips and tricks I find along the way.

Today I was trying to get something that looked nice as a "Preview" box that fades out at the bottom.

I found this extremely useful tip on Stack exchange [here](https://stackoverflow.com/questions/22666063/how-to-fade-the-edge-of-a-div-with-just-css), but I thought it might be nice (for myself later) to explain what exactly is going on.

<!--more-->

<code>
.fadeOutDiv {
  border   : 1px #d8d8d8 dashed;
  position : relative;
}

.fadeOutDiv:after {
  content  : "";
  position : absolute;
  z-index  : 1;
  bottom   : 0;
  left     : 0;
  pointer-events   : none;
  background-image : linear-gradient(to bottom, 
                    rgba(255,255,255, 0), 
                    rgba(255,255,255, 1) 90%);
  width    : 100%;
  height   : 4em;
}
</code>

So, let's break it down...
1. <code>border : 1px #d8d8d8 dashed;</code>
This creates a dashed line around the box. It wasn't really what I was looking for, but it was nice to see where the actual boundary was. Once I saw how it worked, I just deleted it.

2. <code>position : relative;</code>

2. <code>.fadeOutDiv:after </code>


2. <code>content : "";</code>


2. <code>position : absolute;</code>


2. <code>z-index : 1;</code>


2. <code>bottom : 0;</code>

2. <code></code>

2. <code></code>

2. <code></code>

2. <code></code>

2. <code></code>
