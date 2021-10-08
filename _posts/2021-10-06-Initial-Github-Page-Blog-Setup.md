---
title: 'Initial Github Page Blog Setup'
categories:
  - Blog
tags:
  - Github
  - Jekyll
  - Ruby
---

This blog has been setup on [github pages](https://pages.github.com/ "Basic Intro to Github Pages") using [Jekyll](https://jekyllrb.com/ "Jekyll docs") [Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/ "Main page about the theme"). All done on the [Arch OS](https://wiki.archlinux.org/ "Arch Wiki")

> Note: It's been a while since I set up this blog and as such the blog post may be all over the place

**_Always_** be sure to read the documentation carefully. 5-10 minutes properly reading a section saves you hours. It was a pitfall I fell into. I missed the mmistakes theme setup guide mentioning that Github Pages only allow liquid achiving instead of plugins like [jekyll-archives](https://github.com/jekyll/jekyll-archives/ "Github page for the archive plugin").

Something to keep in mind if you are thinking of using the mmistakes theme is the versionning. I had some conflict issues with Jekyll, Ruby and Webrick versions.

I found that the following versions worked for me
  * Ruby 2.7.4
  * Jekyll 3.9.0
  * Webrick 1.6.1

Otherwise, I would get an [error](https://bbs.archlinux.org/viewtopic.php?id=265534 "A thread on the versionning error I got").

If it's your first time using Ruby you might be interested in what exactly is a "gem". A good explanation can be found [here](https://stackoverflow.com/questions/5233924/what-is-a-ruby-gem "What is a Ruby Gem?"). In summary, it's basically a standard format for Ruby programs and libraries.

I installed [Ruby](https://wiki.archlinux.org/title/Ruby#RubyGems "Arch wiki on Ruby") with the [rbenv](https://wiki.archlinux.org/title/Rbenv "Arch wiki on rbenv") as the environment and used RubyGems to install [Jekyll](https://wiki.archlinux.org/title/Jekyll "Arch wiki on installing jekyll") and Bundler

> Note: You need to install ruby-build plugin to use rbenv install

> Remember to setup a [jekyll github token](https://mycyberuniverse.com/fixing-jekyll-github-metadata-warning.html "Guide for setting the token up") for your repo unless you want to get an error.

_Useful command_

`bundle exec jekyll serve --livereload` -> Runs the blog locally with autoupdate turned on.

Those were the couple of things I wanted to jot down. Hopefully, future blog posts will be more structured.
