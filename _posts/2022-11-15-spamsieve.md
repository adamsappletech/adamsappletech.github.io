---
layout: post
title:  SpamSieve - Spam Filtering for Mac
date:   2022-11-15 12:57:06 -0700
categories: Software Review
excerpt_separator: <!--more-->
---

Email spam is an ongoing problem, which seems to be getting worse over time. When I have had the same email address for many years, more and more spam seem to clutter my inbox. Using the same address with shopping online or trying new services and apps, brings with it an increase of junk email. <!--more--> Apple's "[Hide My Email](https://support.apple.com/en-us/HT210425)" service which is available with an iCloud subscription is a great feature for proactively preventing future spam. You can use a unique email address that will forward to your main email address. It is easy to use and if you notice more spam from a specific place, you can go and disable the unique address and those messages sent to that unique address will go away. 

![Spamsieve icon][image-1]

I have used [SpamSieve](https://c-command.com/spamsieve/) by C-Command Software for many years for filtering out the junk email. SpamSieve is an older macOS app, in fact it has been around since the early days of Mac OS X, 20 years or so. In order for SpamSieve to work its best, you need to have an always-on Mac running Mail. In dealing with spam, some services rely on a server running online to filter messages before they reach your Mac, but with SpamSieve the filtering is done locally on your personal computer. This is kind of an "old school" way to do this, but I find that it works great and is more affordable than other online services. 

## Setup

You need to have a Mac running Mail at all times for the filtering to work without interruption. I keep my office computer running for this purpose, but you could also have a Mac mini tucked away in a closet in your house running Apple Mail and SpamSieve. 

As messages come in, SpamSieve evaluates the message and moves it into a specific Mail folder if it thinks it is Spam. The training works great and you can train messages as "Spam" or as "Good". 

It takes a little bit of setup, working with Apple Mail rules and AppleScripts to get the configuration working. I use the rules and AppleScript support so that I can move messages to either a "train good" or "train spam" folder from my iPhone. Those messages will later be processed and trained when they are noticed on the Mac mini. 

## The Last Word

If you don't have a Mac that you can leave running, then you may want to look elsewhere for spam management. A popular online service for this is [SaneBox](https://www.sanebox.com). SaneBox has access to your email accounts online, and processes your spam and other mail rules on the server side, before your Mac downloads any messages. The service has great reviews, but it is significantly more expensive than SpamSieve, with a monthly subscription of at least seven dollars per month. 

SpamSieve is older software, but it has been updated for the latest release of macOS Ventura. It is tried and true for me and still the best way to manage spam email locally on my Mac.

[image-1]: /assets/spamsieve-icon@2x.png

<script src="https://giscus.app/client.js"
        data-repo="adamsappletech/adamsappletech.github.io"
        data-repo-id="R_kgDOK5uboQ"
        data-category="General"
        data-category-id="DIC_kwDOK5uboc4CbzPX"
        data-mapping="pathname"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="bottom"
        data-theme="preferred_color_scheme"
        data-lang="en"
        crossorigin="anonymous"
        async>
</script>