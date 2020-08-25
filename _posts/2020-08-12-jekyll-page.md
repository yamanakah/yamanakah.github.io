---
title: "How to set up a Github page with Jekyll on Windows"
date: 2020-08-14T10:00:00-04:00
categories:
  - Tutorials
tags:
  - Jekyll
  - GitHub
  - blogging
---

Welcome to this quick guide on how to set up a website or personal blog with GitHub pages and Jekyll on Windows. Both services are completely free of any cost, perform very well and can help create great looking sites.

The blog you are on right now was set up by me using the steps outlined below!

The only prerequisite you will need is an account on [GitHub.com](https://github.com){:target="_blank"}.

The first steps are to install Jekyll and create a GitHub repository for the webpage.

## Jekyll installation

Note that Windows is not an officially supported platform for Jekyll. Nevertheless it can be run just fine by following the steps below. The easiest way is by using the RubyInstaller for Windows. It provides the Ruby language and execution environment, which Jekyll runs on.

1. Download the recommended version of the rubyinstaller-devkit
[RubyInstaller Download](https://rubyinstaller.org/downloads/){:target="_blank"}
2. Install the Ruby base files with the "MSYS2 development toolchain"
3. Run the "ridk install" step on the last page of the installation wizard
4. In a new command prompt window run: `gem install jekyll bundler`

## GitHub page repository

Next, you want to create a GitHub repository for the website. Use your `username` plus `.github.io` as the repository name. This will also be the webpage address.

![GitHub repository](/assets/2020-08-12-jekyll-page/github_repo.PNG)

>Note: Replace "username" with your GitHub account name.

If you name the repository anything other than username.github.io it will still work as a GitHub page, but the address will be `username.github.io/repository_name`.

Once the empty repository is created go to the repository `settings` and scroll down to the GitHub Pages section. Here you need to set the source as `branch: master` in your `root` folder.

![repository settings](/assets/2020-08-12-jekyll-page/github_site.PNG)

Now you are all set to create the webpage content.

## Create Jekyll site

For the next steps you will need to use git commands to set up everything locally. I work in VisualStudio Code (VS Code) but you can use any text editor option available to you. Depending on your set up you will need to download [Git for Windows](https://git-scm.com/download/win){:target="_blank"}.

Clone your new GitHub repository on your local environment. In VS Code press `CRTL+Shift+P` and type the command `Git:Clone`, followed by the repository URL (example: `https://github.com/username/username.github.io`).

Open a terminal session and go to the repository - the current directory needs to be the location of the cloned repository. Now create a new Jekyll project by running the following command

```jekyll new . --force```

This will create a number of folders and files inside the repository which will be used to create your webpage later. At this stage the Jekyll site is set up and ready to be explored and edited.

#### Running the site locally
First, you need to install the necessary Jekyll bundles by executing the following command inside the terminal:

```install bundles```

Now the website can be run locally. This will be great for inspecting the content and layout inside your browser. For this you will need to run Jekyll with bundle exec:

```bundle exec jekyll serve```

Once the command executes it will offer a link in the terminal output. Click that link (`CTRL+click` in VS Code) and the webpage will open in your  browser, displaying the locally hosted content.

![local website](/assets/2020-08-12-jekyll-page/local_site.PNG)

Press `Ctrl+C` and type `Y` inside the terminal to stop the running process at any time. Whenever you edit the page content the changes to the website will be visible when reloading the browser.

For a continuous live feed of the latest website state add `--livereload` to the command above. This will set up the local browser page to reload automatically after every saved change:

```bundle exec jekyll serve --livereload```

> #### Troubleshooting livereload under Windows
> Sometimes the livereload functionality does not work under Windows. To resolve the issue you need to re-install the eventmachine gem. In order to do so, run the following two commands:
>
> ```gem uninstall eventmachine --force```
>
> ```gem install eventmachine --platform ruby```
>
>Now run the command `bundle exec jekyll serve --livereload` again. It should work fine.

## Getting the GitHub page online
Once the Jekyll site has been created on the local cloned repository it only needs to be uploaded to GitHub. Commit the changes made locally and sync the repository with GitHub. In VisualStudio Code you can press `CRTL+Shift+P` and type `Git: Commit` followed by `Git: Sync`.

Check on GitHub.com whether your repository updated with the latest changes. The webpage will be automatically created and hosted by GitHub after a short while.

To see the page online go to your specific URL. You can always find it by going to the repository and `settings > GitHub Pages`.
If you followed the steps above your URL should look something like this `https://username.github.io/`.


## Next steps
#### Changing the website theme
By default the Jekyll page uses the [minima](https://github.com/jekyll/minima){:target="_blank"} theme. It is a beautiful and simplistic layout but does not offer many customizable features. Luckily there is a big community around Jekyll websites that offers plenty of alternative themes.

Take a look at the following resources to get some inspiration. The instructions on how to set up the different themes is usually well documented.

- [Official GitHub Pages supported themes](https://pages.github.com/themes/){:target="_blank"}

- [Jekyllthemes.io](https://jekyllthemes.io/){:target="_blank"}

- [Jekyll-themes.com](https://jekyll-themes.com/){:target="_blank"}

- [Jekyllthemes.org](http://jekyllthemes.org/){:target="_blank"}

>Note: Make sure the theme is supported by GitHub pages.


#### Further reading

There is a lot of good information out there on how to set up, customize and build on the simple first GitHub page created here. The best place to start is the official Jekyll site. It offers resources on themes, plugins, content mangament, etc. It even has community created tutorials on different subjects. Take a look at:

[https://jekyllrb.com/resources/](https://jekyllrb.com/resources/){:target="_blank"}

If you want to read more about GitHub pages then the best starting point will be the official guide on GitHub.com:

[https://docs.github.com/en/github/working-with-github-pages](https://docs.github.com/en/github/working-with-github-pages){:target="_blank"}



-----
>
> This blog post will be updated and improved on periodically.
>
> Author: Hyoson Yamanaka