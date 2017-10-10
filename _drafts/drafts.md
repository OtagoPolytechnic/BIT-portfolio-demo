---
layout: post
title: Drafts
tags: workflow
---
I'm using [Jekyll's draft post feature](https://jekyllrb.com/docs/drafts/) as part of my workflow because it allows me to initialise a whole lot of related posts and set them up to receive content at a later stage. Once those are finished I can use a [Jekyll::Compose](https://github.com/jekyll/jekyll-compose) command to simply and easily publish them. That will shift them into the `_posts` directory and add the date automatically.

This is great, because it means that I can use `bundle exec jekyll serve --drafts` to view my local dev site in a browser as though all the drafts had been published. This lives on my master branch and I push all changes to GitHub as though it's a dev branch. There's a reason for that: the live site is on the gh-pages branch. I chose that rather than a docs directory to publish my site because it just seems more logical to me. The live site, powered by GitHub Pages, will never show drafts, so I can comfortably pull from master (not natural, but hey) without half-finished work being handed in or made viewable.

I'm going to leave this post at draft status, so you'll only see it in my source code. Sneaky. To see it in a browser, you'd have to fork and clone this repo and then either move the post yourself and serve the site locally, or use the drafts flag as above.

So, if you've found this post, well done! Now you can see how I'm using drafts and exactly what effect that has, as well as gain another insight into my workflow.