---
layout: post
title:  "Hello World"
date:   2017-09-27
categories: test demo
---
This post was actually published on Wednesday 27th at about 11.13am.

The date now is  {{ "now" | date: "%Y-%m-%d %H:%M" }}

Today we tried out installing Jekyll on Windows 10 with deep freeze. There were some things that happened, so that will be the subject of another post. Jekyll is a bit easier to use if you are using a UNIX system (i.e. a Mac) with all the required stuff already on it, but it still worked pretty quickly on Windows.

I am developing this site in my H: drive and version controlling using git. I plan to use GitHub Pages to host it. You should be able to see my progress if you look in the commit history. The first mistake I made was initialising the repo on GitHub first, and then plonking a new Jekyll project in it after cloning it. This just got me a Jekyll directory *inside* a git repo, which was a pain. It wasn't too hard to fix: I just moved the files up one. In hindsight, I should have run `jekyll new <sitename>` first and then initialising and pushing it next.

I've also been looking a bit more into Liquid, which is the language you use to include basic variables and logic and stuff in your site. No php required! The date above (on the second line) is generated using `{{ "now" | date: "%Y-%m-%d %H:%M" }}` and there are lots of ways to create and use your own site-specific code.