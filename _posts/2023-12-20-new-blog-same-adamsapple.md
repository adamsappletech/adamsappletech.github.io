---
layout: post
title:  New Blog - Same adamsapple
date:   2023-12-20 03:56:49 -0700
excerpt_separator: <!--more-->
---

One the reasons I started this website was for the opporunity to learn [Wordpress](https://wordpress.com/). I have tried a few different hosts over the years and I have a better understanding of the pros and cons of Wordpress. <!--more--> I use Squarespace for another website and I like it's design and ease of use, but I don't like to use their mobile app for posting and updating content. With adamsapple I wanted a setup that had the following features: 

- text-based, writing in [Markdown](https://daringfireball.net/projects/markdown/syntax)
- easy to update from my Mac and from mobile (iOS)
- Simple design, fast loading
- inexpensive 

Wordpress checked most of these boxes, but had a fair amount of complexity. Mamy hosting sites have an inexpensive first year cost, but over time the prices go up consierably. A Wordpress project is also pretty fiddly, with a lot of settings and plugins to install. You can post from mobile apps, but they aren't ideal for what I wanted. 

Last month it became necessary for me to move away from Wordpress. I was not optimistic about finding another solution that met the all of the goals above. I didn't have a backup of my website that would be easy to migrate to something else. I had my Markdown files, but I knew that this would proably be a painful transition. 

I have been a reader of Brett Terpstra for many years. Brett is a genius programmer and innovator in the Apple community. His website, [brettterpstra.com](https://brettterpstra.com), again provided me with inspiration. Brett's site is based on [Jekyll](https://jekyllrb.com). I hadn't heard of Jekyll, but I was quickly won over with it's ease of use and flexibility. I also learned about [GitHub Pages](https://pages.github.com). I have been a GitHub user for my programming version control, but I was unaware of GitHub Pages. After a few days of work, adamsapple is now completely setup with Jekyll and GitHub Pages. 

## My Process

Getting started with Jekyll required me to also get more comfortable using the Terminal. This was fine with me, because I wanted an excuse to use the Terminal more. Jekyll requires the following: 

- Ruby version 2.5.0 or higher
- RubyGems
- GCC and Make

I am not a Ruby user and I had to do a little digging to find out what version of Ruby was already installed on my Mac, and I didn't have experience installing Ruby Gems. After a bit of tinkering in the Terminal, it was mostly working, but I was still getting a few errors. I later learned that the version of Ruby that comes pre-installed is an early version of Ruby. As I got further down the road on this project, it became clear that I needed a more recent version of Ruby. This can get sticky fast, and require a significant amount of time in the Terminal, with many possible problems. I found an easier solution called [Ruby on Mac](https://www.rubyonmac.dev). While this isn't a free solution, I feel like the cost was worth it for me. Ruby on Mac takes care of the heavy lifting for getting a functional Ruby install. They pitch it like this: 

> Without Ruby on Mac: Spend days trying to get your Rails, Jekyll, iOS, Flutter, React Native, Unity, Cocoapods, or other Ruby project working. With Ruby on Mac: Run a single command and you'll be up and running in 15 minutes or less.

Afer I installed Ruby on Mac, my error messages went away and I was on my way to starting to configure Jekyll. 

> Jekyll is a static site generator. It takes text written in your favorite markup language and uses layouts to create a static website. You can tweak the site’s look and feel, URLs, the data displayed on the page, and more.

With a static-site generator, like Jekyll, I can have a folder of text files on my Mac, easily edit them with Markdown, and build them into a blog with a short Terminal command. This was looking very promising. The documentation at [https://jekyllrb.com/docs/](https://jekyllrb.com/docs/) was straighforward and easy to follow. 

### Design

Once I had the basic blog setup, I started to think more about design and wanted to see how flexible Jekyll is with the look of the site. I found many free themes to choose from, and found one that I liked called [Plainwhite](https://github.com/samarsault/plainwhite-jekyll). In addition to a clean and simple look, Plainwhite also had the following features: 

- Toggle for changing from light to dark mode
- Responsive to mobile screen sizes
- SEO
- Search Bar
- Excerpts 
- Categories

Many of these features are implemented by a simple one line in the configuration file, and others took a bit more work to get working. 

### Hosting

Once I had a basic design that I liked, I didn't want to get too far in before looking into my hosting options. I didn't have to look far because on the Jekyll documentation site, they advertise the fact that they are "Proudly hosted by GitHub Pages." I have used GitHub for years as my version control remote for my iOS apps, but I didn't know about [GitHub Pages](https://pages.github.com). This is awesome. I can make an account and setup a public repository and push my Jekyll folder to GitHub and now my blog is online. It supports custom domains as well. So far, it has been rock solid. My previous two Wordpress hosts would go down pretty regularly. I would get notified multiple times a week or month that my site was unreachable. So far so good with GitHub Pages. Since it is GitHub, I can also access my live site from my iPhone. (More on this later.)

The setup is pretty straightforward to setup GitHub Pages. If you are going to access your repository from the Terminal or with 3rd-Party GitHub clients, you do need to setup SSH Keys to get the connections to work. 

### Mobile Blogging Setup

Being able to blog from my iPhone and iPad is exciting and liberating. I like the idea of being able to draft ideas from anywhere, and being able to fix small errors from my phone. 

Here are the mobile apps that I have decided on for blogging on the go: 

- [1Writer](https://1writerapp.com) - Markdown editor for iPad and iPhone, with Dropbox folder support. 
- [Working Copy](https://workingcopy.app) - GitHub Client
- [Dropbox](https://www.dropbox.com)
- [Google Analytics](https://marketingplatform.google.com/about/analytics/)
- [Photomator](https://www.pixelmator.com/photomator/)
- [Annotable](https://moke.com/annotable/)

There are many Markdown editors for iOS. Unfortunately, none of them are perfect.[^1] I wanted one that had Dropbox support built in. This is harder to find than you would think. [1Writer](https://1writerapp.com) works great for adding a folder from Dropbox and editing those files directly. I have an old version of TextExpander still installed on my iOS devices and it still integrates well with 1Writer for text snippets. This is great, because Jekyll uses a specific format with front matter for blog posts. 

```
---
layout: post
title:  
date:   2023-12-20 11:53:03 -0700
categories: 
excerpt_separator: <!--more-->
---
```

[Working Copy](https://workingcopy.app) is a very nice GitHub client for accessing, committing, pulling, and pushing your repositories on GitHub. It isn't free but it is very well designed. I can get access to any file on my website and make quick corrections or edits and then push them back to GitHub and they will go live momentarily. 

My favorite photo editor is Pixelmator Pro on the Mac. On iOS, they now have [Photomator](https://www.pixelmator.com/photomator/). This is great for editing photos and screenshots. However, if I want to quickly annotate a screenshot, or blur out some text, I like an app called [Annotable](https://moke.com/annotable/). It is one of those apps that does one thing well. 


### Odds and Ends

There were a couple of blog features that I had to work a bit harder to make work. While Plainwhite technically supports a search bar, comments, and RSS feeds, I had to customize and add these features in another way. I also added Google Anayalitcs to my website as well. This is the beauty of working with text files and HTML files directly. If you can work with a bit of code, you can customize anything you want. 

I have used Disqus in the past, and there is technically built-in support for Disqus in Plainwhite and Jekyll, but I couldn't get Disqus to connect. Instead, I found out that GitHub has a commenting service called [Giscus](https://giscus.app). With just a few lines in my config file, and a script for each blog post, I was up and running with comments. 


### Not The Last Word

So far, I am super happy with my new setup. It is much simpler than Wordpress, faster to load, hasn't gone down yet, is free (except for my custom domain), and very mobile friendly. 

In this whole process I also want to give an honorable mention to the fanstastic text editor [Sublime Text](https://www.sublimetext.com). I had heard of Sublime Text, but never tried it. It is a beautiful text editor with a two panel design. I can keep my most-used folders on the left and then edit text on the right. It has syntax highlighting for many languages, including Markdown. It has been a joy to use. 

There is more to come on adamsapple...


[^1]: See [Jason Snell's article](https://sixcolors.com/post/2021/03/searching-for-the-perfect-ios-markdown-writing-tool/) about this very topic. 


{% include comments.html %}