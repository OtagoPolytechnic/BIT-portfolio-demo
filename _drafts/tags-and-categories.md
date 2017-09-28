---
layout: post
title: Tags and categories
categories: technical
tags: jekyll demo test
date: 2017-09-29
---
Today I'm finding out about how to deal with post tags and categories. These are defined in front matter and I want to use these to organise posts in my portfolio. I'll use categories to populate the main navigational pages that relate to the marking schedule, such as projects, technical proficiency and professional proficiency (ok, the latter is actually an element of the software engineering marking schedule, but why not kill two birds with one stone?).

Firstly, categories can be accessed via an inbuilt Jekyll Liquid variable: {% raw %} `{{ page.categories }}` {% endraw %}. I have decided to have a page listing each post in the main categories, so I'm looping over just the posts in that category. I just modified the for loop in the home page template (it's in the minima template files, which are tucked away somewhere). It grabs all posts, so I changed it to just grab the ones from the right category.

Fot tags, I'd like to make a tag cloud. That's a pretty common thing to have in a blog, but there's a bit of work to do if you want one in Jekyll. I'm following [this tutorial](https://superdevresources.com/tag-cloud-jekyll/) to work it out. Tags are also specified in front matter, so that bit is pretty easy. The code given in the tutorial needs almost no tweaking, but I did add a [Liquid](https://shopify.github.io/liquid/) trick to remove the white space so that my tags sit inline instead of in a big, spaced out list.

I encountered a problem where all my random tag pages ended up in my main nav at the top, which makes it all very messy. I found a Stack Overflow thread about excluding pages from the main nav, but came up with a much simpler method myself: I copied the `header.html` page from the `_includes` folder in the template files into my own includes folder, and just made one little change to the `if` statement in order to make use of a front matter tag `nav: true` on pages I want in the nav. Easy!  