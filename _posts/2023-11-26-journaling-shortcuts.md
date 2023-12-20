---
layout: post
title:  Automate Journaling Day One with Shortcuts
date:   2023-11-26 05:47:12 -0700
categories: Productivity
excerpt_separator: <!--more-->
---


I am not a natural journal writer, and I am a nerd who likes to program as a hobby. So, it seems natural that I could combine these two traits and use Apple Shortcuts to automate a daily journal entry for me in my favorite journaling app, [Day One][1]. I used to accomplish this only with AppleScript, with inspiration and help from [Brett Terpstra][2]. <!--more--> My old AppleScript relied on a command-line utility called [iCalBuddy][3]. I recently got a new computer and I had trouble getting iCalBuddy to work, so I decided to redo my automation using Apple Shortcuts. In the end, I think this is even better than my original script. It still relies on some AppleScript, and so it won’t run on iOS, but so far it has been rock solid. 

This shortcut finds my calendar events for today and puts them into a list, organized by calendar. It then looks at my to do list in [Things][4], and makes a list of the tasks that I completed today. Finally, it accesses a CNN RSS feed to find today’s top headlines, puts the title in a list, with a link to the article. 

I can then add a picture to the journal entry, or add a longer text reflection, if I want to personalize it further. I use Keyboard Maestro to run the Shortcut at a certain time each night. Day

## Shortcut

The Shortcut relies on the following:

Day One actions: 

- Create New Entry
- Append to Entry

Calendar actions: 

- Find Calendar Events Where

Things actions: 

- Find Items Where

AppleScript Action: 

- Run AppleScript

General Action: 

- Replace Text


![Journal Script 1][image-1]

![Journal Script 2][image-2]

## AppleScript

Here is the AppleScript I use to get the daily headlines. 

        property RSSURL : "https://rss.nytimes.com/services/xml/rss/nyt/HomePage.xml"
        on run {input, parameters}
                set ASTID to AppleScript's text item delimiters
                set AppleScript's text item delimiters to {("<item>" & (ASCII character 13))}
                try
                        do shell script "curl -sS " & quoted form of RSSURL
                        set rssFeed to every text item of result
                        set AppleScript's text item delimiters to ASTID
                        
                        if (count rssFeed) is greater than or equal to 6 then
                                set rssFeed to items 2 thru 6 of rssFeed
                        else
                                set rssFeed to items 2 thru (count rssFeed) of rssFeed
                        end if
                on error errorMsg number errorNum
                        set AppleScript's text item delimiters to ASTID
                        display dialog "Error (" & errorNum & "):" & return & return & errorMsg buttons "Cancel" default button 1 with icon caution
                end try
                
                
                delay 2
                set newsList to {}
                repeat with thisPiece in rssFeed
                        set newsList's end to (text 8 thru -9 of (first paragraph of thisPiece))
                        set newsList's end to (text 14 thru -8 of (third paragraph of thisPiece))
                end repeat
                return newsList
        end run

Writing a meaningful, personalized, journal entry each day is likely better for your mental health, but if you are like me and find it difficult to journal daily, but want a daily record, this shortcut may be helpful to you. It reminds me to reflect on my day, and on important days I do remember to go back and write the more meaningful reflection. 

{% include social-media-share.html %}

[1]:    https://dayoneapp.com
[2]:    https://brettterpstra.com
[3]:    https://hasseg.org/icalBuddy/
[4]:    https://culturedcode.com/things/

[image-1]: /assets/journal-script-1.png
[image-2]: /assets/journal-script-2.png

{% include comments.html %}