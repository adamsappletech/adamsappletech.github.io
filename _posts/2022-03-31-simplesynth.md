---
layout: post
title:  SimpleSynth - Quick MIDI Keyboard for macOS
date:   2022-03-31 04:49:24 -0700
categories: QuickTip macOS Music Software
excerpt_separator: <!--more-->
---

I have a midi keyboard connected to my desktop computers. It is great to be able to quickly enter notes into [Finale](https://www.finalemusic.com), or experiment in [Logic](https://www.apple.com/logic-pro/) or [GarageBand](https://www.apple.com/mac/garageband/). However, sometimes I just want to play a few notes or practice some piano without launching a large app like Logic. <!--more--> With larger apps like Finale or even GarageBand, I have to start a new project and am presented with many settings for tempo and key signature. This provides just enough friction for me to procrastinate my practice. I need to be able to enable sounds on my MIDI keyboard with one click and get to the playing. Enter [SimpleSynth](https://github.com/lllucius/simplesynth64). 

![SimpleSynth Icon][image-1]

SimpleSynth is a very lightweight app, which simply gets MIDI sounds out of my connected MIDI keyboard. It doesn't record, the layout isn't fancy, but it launches fast and allows me to choose the MIDI sound that I want with the least amount of friction. 

When I switched to Apple Silicon with my new MacBook Pro 14" M1 Max, SimpleSynth stopped working for me. It hadn't been updated for 64 bit. Luckily, it has been updated on Github as SimpleSynth64. 

Thank you to [Pete Yandell](http://notahat.com/simplesynth) for originally writing the app and for [rraallvvv ](https://github.com/rraallvv/simplesynth.git) on Github for releasing this new version.

{% include social-media-share.html %}

[image-1]: /assets/simplesynth_icon.png

<style type="text/css">
    img {
        display: block;
        margin-left: auto;
        margin-right: auto;
        width: 250px;
    }
</style>

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