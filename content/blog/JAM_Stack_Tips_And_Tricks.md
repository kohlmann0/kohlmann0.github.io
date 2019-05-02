---
title: "Jam Stack - Tips and Tricks"
date: 2018-03-13T14:08:04-05:00
draft: true
---



With HUGO and writing in Markdown, it's just faster to focus on the writing, rather than worrying about all the HTML tags, and avoid problems with missed closing tags, css, etc. If you get it setup well the first time, every time after that is simply exploring what you want to say, rather than nit-picking the code, or how it looks. It will look the same (hopefully great) every time.



With HUGO, you have the ability to create "partials", which is exactly as it sounds. Basically modular components, that you can reuse whenever you want. Helps you with the best practice of Don't Repeat Yourself. Write it once and reuse it everywhere... HUGO will insert it wherever it needs to go... just keep in mind your opening and closing tags. Try to keep them matched, within the same partial, or you'll have to remember to close it later in your code.



Hugo gives you a local build server which is great for debugging and seeing what the final result will be, before you commit it to github. What's awesome is that it monitors changes within your site, as you are coding, and rebuilds it automatically whenever it sees a saved change. You don't have to manually rebuild your changes every time. The rebuild times are super fast too. Like 25ms, because it's only updating the difference, not the whole site.



With Netlify you can have your website rebuilt every time you check in changes to github. Netlify monitors your repository, and then rebuilds it after every checkin. What's awesome about that is that you don't have to have your Development machine with you, in order to update your site. You know how you can edit a markdown file right on the github site? Find your minor change, update it where ever, commit the change, and the whole site will compile and rebuild... Also, it's free! How can you go wrong?

