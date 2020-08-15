---
title: "How to set up a Github page with Jekyll on Windows"
date: 2020-08-14T10:00:00-04:00
categories:
  - blog
tags:
  - Jekyll
  - GitHub
  - tutorial
  - blogging
---

>This post is a work in progress! 

Here is a quick guide on how to set up a website or personal blog with GitHub pages and Jekyll. Both platforms are completely free of any cost, perform very well and can be foundations for great looking sites.

## Jekyll installation

Note that Windows is not an officially supported platform for Jekyll. Nevertheless it can be run just fine by following the steps below. The easiest way is using the RubyInstaller for Windows. It provides the Ruby language and execution environment, which Jekyll runs on.

1. Download the recommended version of the rubyinstaller-devkit 
[RubyInstaller Download]("paste link here")
2. Install the Ruby base files and MSYS2 development toolchain
3. Run the "ridk install" step on the last page of the installation wizard
4. In a new command prompt window run: "gem install jekyll bundler"

## GitHub page repository

Quick guide for setting up a webpage with GitHub pages and Jekyll on a Windows environment.
Create a Github repository for the websites content on Github.com and clone it on your machine.

Go to the repository and create a new Jekyll project > jekyll new . --force

Install bundles

In order to look at the website via your browser type > bundle exec jekyll serve. Press Ctrl+C to stop the process. Any changes to the website will be visible when reloading the browser. For a continous livefeed of the latest website state add --livereload to the command.

## Making livereload work on Windows
To resolve the issue with the livereload you need to re-install the eventmachine gem. In order to do so, run the following two commands:
Uninstall eventmachine
1. $ gem uninstall eventmachine --force
2. $ gem install eventmachine --platform ruby


-----
Sources:
jekyllrb.com
github.com