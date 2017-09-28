---
layout: post
title:  Hello World
date:   2017-09-27
tags: test demo git workflow
categories: technical
---
This post was actually published on Wednesday 27th at about 11.13am.

The date now is  {{ "now" | date: "%Y-%m-%d %H:%M" }}

Today we tried out installing Jekyll on Windows 10 with deep freeze. There were some things that happened, so that will be the subject of another post. Jekyll is a bit easier to use if you are using a UNIX system (i.e. a Mac) with all the required stuff already on it, but it still worked pretty quickly on Windows.

I am developing this site in my H: drive and version controlling using git. I plan to use GitHub Pages to host it. You should be able to see my progress if you look in the commit history. The first mistake I made was initialising the repo on GitHub first, and then plonking a new Jekyll project in it after cloning it. This just got me a Jekyll directory *inside* a git repo, which was a pain. It wasn't too hard to fix: I just moved the files up one. In hindsight, I should have run `jekyll new <site_name>` first and then initialised and pushed it next.

I've also been looking a bit more into Liquid, which is the language you use to include basic variables and logic and stuff in your site. No php required! The date above (on the second line) is generated using {% raw %} `{{ "now" | date: "%Y-%m-%d %H:%M" }}` {% endraw %} and there are lots of ways to create and use your own site-specific code.

BTW, to get that snippet of Liquid code to display instead of run was a bit of a task. I found the answer in this [GitHub issue](https://github.com/jekyll/jekyll/issues/4650).

My development workflow is to work on `master` for content updates, with a dev branch for major layout/theme/site structure changes. The work will be done mostly on my H drive, using `jekyll serve --draft` to send changes live to my browser for local development and testing. Finished drafts can then be published locally, and then finished version of the site will be pushed to a gh-pages branch for public viewing.

This is about as long as a useful post should get, so check out the post about getting Jekyll running on Windows for more interesting reading (I mean more reading that's interesting, not reading that's more interesting).

PS: I'm using [Jekyll::Compose](https://github.com/jekyll/jekyll-compose) to streamline the post and page publishing process.