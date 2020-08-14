---
title: "How to set up a Github page with Jekyll on Windows"
date: 2020-08-12T15:00:00-04:00
categories:
  - blog
tags:
  - Jekyll
  - GitHub
  - websites
  - tutorial
---

Create a Github repository for the websites content on Github.com and clone it on your machine.

Go to the repository and create a new Jekyll project > jekyll new . --force

Install bundles

In order to look at the website via your browser type > bundle exec jekyll serve. Press Ctrl+C to stop the process. Any changes to the website will be visible when reloading the browser. For a continous livefeed of the latest website state add --livereload to the command.

## Making livereload work on Windows
Uninstall eventmachine
$ gem uninstall eventmachine --force

Re-install eventmachine
$ gem install eventmachine --platform ruby