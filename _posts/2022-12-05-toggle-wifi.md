---
layout: post
title:  Toggle WiFi On and Off
date:   2022-12-05 01:02:26 -0700
categories: QuickTip
excerpt_separator: <!--more-->
---

I am coming up on my one-year anniversary with my M1 Max 14-inch MacBook Pro. It is the best computer I have ever used. It is so fast and a powerhouse in every way. I use it for Xcode, Final Cut Pro, music production, and it always delivers.

<!--more--> However, computers are not without little hiccups here and there. Lately, I have had some battery issues when it is asleep. I am sure there is some little app that has been preventing my MacBook Pro from sleeping. When I have reached into my bag to get it out, it has been noticeably warm and the battery is depleting when it should be asleep. In all fairness to the computer, I do run a lot of apps and my menu bar is embarrassingly filled with running applications.[^1]

I am still not certain which process has been causing the heat and battery issues, but I did recently find an interim solution. With a short shell script and [Keyboard Maestro](https://www.keyboardmaestro.com/main/), I can quickly disable WiFi before I close the lid. This has immediately brought back amazing battery life and my computer is super cool when I pull it out of my bag.

The script for toggling WiFi in the Terminal is:

```
networksetup -getairportpower en0 | grep "On" && networksetup -setairportpower en0 off || networksetup -setairportpower en0 on

```

I setup a [Keyboard Maestro](https://www.keyboardmaestro.com/main/) hotkey to quickly toggle the WiFi on and off.

![Keyboard Maestro Screen][image-1]

I love the Mac.

{% include social-media-share.html %}

[^1]: Thank you [Bartender](https://www.macbartender.com) for keeping my menu bar manageable. (Also a part of [Setapp](https://setapp.com))

[image-1]: /assets/toggle-wifi-keyboard-maestro.png


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