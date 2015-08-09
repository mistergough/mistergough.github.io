---
layout: post
title: Static Blogging
date: 2015-08-09
categories: []
tags: []
status: publish
type: post
published: true
author:
  email: mistergough@gmail.com
  display_name: mistergough
  first_name: Simon
  last_name: Gough
excerpt: !ruby/object:Hpricot::Doc
  options: {}
comments: true
---
Over the past couple of days I've been moving this blog from its original [Wordpress.com](https://mistergough.wordpress.com) version to a static blog.

Static blogs don't use a database. The HTML files are generated at the point of creation rather than dynamically generated at the point of viewing. The most obvious advantage of this is speed for the reader, but there are side benefits too, such as better security and fewer management requirements.

There are lots of ways to generate static files, including the completely manual approach, but for this blog I decided to use  [Jekyll](http://jekyllrb.com/). Jekyll is a processing application that pulls together separate files and combines them into finished HTML pages. The point of this it to make it easier to separate content and presentation so that blog posts can be written in, say, [Markdown](http://daringfireball.net/projects/markdown/), just as with this one. It also means that you can reuse snippets of HTML in lots of places, such as page headers and footers.

Anyway, for an overview of Jekyll [take a look at the website](http://jekyllrb.com/).

Another reason for using Jekyll is the fact that it's supported by [Github Pages](https://pages.github.com/), a simple website hosting platform that works from a dedicated Github repository. For free.

There are many different ways to set up a Jekyll and Github blog, and the right approach will depend largely on personal preferences, but [this page](https://pages.github.com/) should give you an idea of what's involved.

The first step is to get a Github account, if you don't already have one. Once you have an account you can set up Github Pages as a dedicated respository.

After this you should clone the remote repository to your local computer. Github provides full instructions for this. Scrolling down [this page](https://pages.github.com/) you'll find instructions for getting Jekyll up and running. This can be a bit fiddly but what you want to end up with is jekyll running on your local computer for generating static files and enough of an understanding of git to push those files up to the Github repository.

Once you have the basics working you can play around with design, structure and content. Every update, whether it's a design change or new post becomes a matter of pushing the modified files to your repository.

### CSS

Jekyll has built in support for [CSS extension Sass](http://sass-lang.com/), which is well worth learning and using if you don't already. Of course, if you don't want to get into the design side at all you can just download and use ready made themes ([Jekyll Bootstrap](http://jekyllbootstrap.com/) is worth a look). You can even use the theme I've built here by cloning all the site files [from my own repository](https://github.com/mistergough/mistergough.github.io).

### Markdown

Markdown is a simple system for styling text documents. Jekyll has built-in support for Markdown which means that you can write your posts in a more user-friendly way and then let Jekyll handle the rest. It's worth learning the [Markdown syntax](http://daringfireball.net/projects/markdown/) as it's become something of a standard.

### Commenting

The biggest drawback to Jekyll at this point is the lack of any good static commenting systems. At this point [Disqus](https://help.disqus.com/customer/portal/articles/472138-jekyll-installation-instructions) remains the most effective commenting system. It's pretty easy to set up even if it's not to everyone's taste.

### Importing

Moving a blog from another platform turned out to be easier than I expected. Jekyll has lots of [import extensions](http://import.jekyllrb.com/) for just about every major blogging system and moving posts here from Wordpress.com turned out to be pretty painless. The only snag turned out to be transferring images so if you have a lot of those you might need to put a bit more work in.

### Feeds

Site feeds turn out to be pretty simple too. You can use the [feed.xml](https://github.com/mistergough/mistergough.github.io/blob/master/feed.xml) template in my own repository without too much configuration or look around for other people's. There are plenty out there.

So, if you like the look of this blog just take what you want and modify accordingly. I'd love to know how you get on.

### Difficulty

I mentioned at the beginning of this post that I'd spent a couple of days doing this. OK, not full time, but if you're new to some or all of the technologies here the whole process of setting up a Jekyll blog might take some effort. However, there's a lot to be said for using static files for simple sites. Plus Git, Jekyll, Markdown and Sass (and the command line if you choose to go down that route) are all good things to get to grips with. So, yes, it might not be the easiest way to get a blog up and running but it's definitely worth a go.
