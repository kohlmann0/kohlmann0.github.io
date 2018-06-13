---

title: "JAM Stack_An_Introduction"

date: 2018-03-13T14:07:37-05:00

draft: true

---



#The Jam Stack

What is the Jam Stack, and how does it differ from other technology stacks?



###First... what does JAM stand for?

J - JavaScript

A - API's

M - Markdown or Markup



Unlike some technology stacks that run server side code to generate a page (like asp.net, PHP, or Java), the Jam Stack is all client side code. Meaning it's all static HTML pages, with JavaScript making calls to API's doing any dynamic content it needs. That doesn't mean you can't still static site generators to template and build pages from components, but the end result is a file, just like any other HTML file, that gets served up from the server. The difference is that it's all pre-built, not generated server-side on the fly.



###Here's an example...

This site itself is considered a JAM Stack. I use a static site generator called Hugo. I created several template files to create a common layout of for this blog, and then markdown files to write the content quicker than I can in markup. Then Hugo compiles the to into individual HTML, JavaScript and CSS files. Then I commit it to Github which serves up the files for free at kohlmann0.github.io. One advantage to this, is that Netlify.com will give you a custom domain name for free, and github will take this, and serve up your website, under your new custom domain, like www.michaelkohlmann.com.



All completely free, expandable, and still dynamic through JavaScript and Dom manipulation.



###Some tips and tricks from building this site...

With HUGO and writing in Markdown, it's just faster to focus on the writing, rather than worrying about all the HTML tags, and avoid problems with missed closing tags, css, etc. If you get it setup well the first time, every time after that is simply exploring what you want to say, rather than nit-picking the code, or how it looks. It will look the same (hopefully great) every time.



With HUGO, you have the ability to create "partials", which is exactly as it sounds. Basically modular components, that you can reuse whenever you want. Helps you with the best practice of Don't Repeat Yourself. Write it once and reuse it everywhere... HUGO will insert it wherever it needs to go... just keep in mind your opening and closing tags. Try to keep them matched, within the same partial, or you'll have to remember to close it later in your code.



Hugo gives you a local build server which is great for debugging and seeing what the final result will be, before you commit it to github. What's awesome is that it monitors changes within your site, as you are coding, and rebuilds it automatically whenever it sees a saved change. You don't have to manually rebuild your changes every time. The rebuild times are super fast too. Like 25ms, because it's only updating the difference, not the whole site.



With Travis C.I. (Continuous Integration) you can have your website rebuilt every time you check in changes to github. Travis monitors your repository, and then rebuilds it. What's awesome about that is that you don't have to have your Development machine with you, in order to update your site. You know how you can edit a markdown file right on the github site? Find your minor change, update it where ever, commit the change, and the whole site will compile and rebuild... Also, it's free! How can you go wrong?



###Javascript, API's and Dom manipulation make it dynamic..