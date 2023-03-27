---
layout: blog-post
title: Trials and Tribulations Working With Jekyll
date: 2023-03-27 20:00:00 -0500
webmentionsEnabled: true
tags: [blog, technology, jekyll, ruby]
---
Working on this site has been a great reintroduction to authoring content for the web.
CSS feels like a completely different beast with animations, variables, and calculations!
Using Jekyll has also really made the authoring process so much smoother; however, this is where I think I've run into the most trouble. Before this project, I had never used Ruby and I had no idea how easy it was to break Ruby environments 😆.
Sure, creating a simple Jekyll project and publishing it on AWS was easy enough. That's when I decided to automate the process with Github actions and ran into my first problem: the local Ruby version. Simply not managing the Ruby version in either the development or build environments immediately created compatability issues. Sure, ok. I'll just pin the Ruby version in the Github action and be done, right? Great!
Now, I want to add Webmentions to my site, which brought me to my next major issue: Ruby versions and Gem compatability.
I've spent a lot of my career so far working primarily in Python, so I'm no stranger to weird compatability issues and dependency hell, but somehow Ruby makes it even harder. It wasn't until I managed to completely trash my environment that I finally discovered rbenv. One complete environment teardown later I think I've finally got everything working the way it should.
Next up... The blog landing page perhaps? 🤔