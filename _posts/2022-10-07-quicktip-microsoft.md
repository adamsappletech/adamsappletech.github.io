---
layout: post
title:  Error Message in Microsoft Office
date:   2022-10-07 11:48:40 -0700
categories: QuickTip
excerpt_separator: <!--more-->
---

I had a weird Microsoft Office bug a few months back. Every time I would open Word or Excel I would get this error in a dialog box: 

```
Microsoft Visual Basic Run-time error `53'
File not found: /Libary/Application Support/Adobe/MACPDFM/MacPDFM.framework/Versions/A/MacPDFM

```

I would dismiss it, but it would return every time I opened a file or started the app. It got to be very annoying after a while. Fortunately, there is a fix. <!--more--> 

1. Close all Office applications.
2. Go to /Users/your-user-name-here/Library/Group Containers/UBF8T346G9.Office/User Content/Startup/Word.
3. Remove linkCreation.dotm.
4. Restart Word and problem solved.

This should fix the problem for Microsoft Word, but a few additional steps are needed for Excel and Powerpoint: 

1. Remove the SaveAsAdobePDF.ppam and SaveAsAdobePDF.xlam from the PowerPoint and Excel folders next to the Word folder.
2. Launch Excel and PowerPoint and go to the menu Tools -> Excel Add-ins... and Tools -> PowerPoint Add-ins..., respectively, and remove the Save as Adobe PDF add-in, by unchecking it and removing it with the "-" button and then click OK.
3. Restart Excel and PowerPoint and the problem should go away. 

This fix has really saved my sanity. 

{% include social-media-share.html %}

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