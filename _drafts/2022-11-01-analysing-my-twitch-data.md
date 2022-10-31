---
title: Analysing my in-depth Twitch data export, and how you can too!
author: Jake Lee
layout: post
image: /assets/images/2022/twitch-header.png
tags:
    - Twitch
    - Calculations
    - Data
---

INTRO

All of the calculations used in this post [are available in a spreadsheet](https://docs.google.com/spreadsheets/d/16bE6egEtML9t6rPVaqtLMZU7pPjixSlmG_JhVQ0dJkY/edit?usp=sharing), feel free to look at how the data is calculated.

## Getting your data

First things first, there might be a delay here. There was an astonishing *6 month delay* between my data request and actually receiving my data!

### Request your data

There's unfortunately no easy way to export your data from Twitch, so you'll have to [fill in their Data Access Request Form](https://www.twitch.tv/p/en/legal/privacy-choices/#:~:text=hold%20about%20you%2C-,submit%20your%20request%20here.,-You%20will%20need) (linked from [Privacy Choices](https://www.twitch.tv/p/en/legal/privacy-choices/)), providing verification that you own the account you are requesting data from.

| Request & response | Request |
| --- | --- |
| [![](/assets/images/2022/twitch-request-thumbnail.png)](/assets/images/2022/twitch-request.png) | Hey,<br><br>I'd like to export as much of my Twitch account data as possible please. Ideally this would include:<br>- Chat messages sent<br>- Viewtime per channel (live + VOD)<br>- Channel subscription history<br>- Any other user data you have immediately available<br><br>Thank you very much! |

### Download your data 

When your data is finally ready, you will receive an email title "Your Privacy Request Needs Attention". After following the link and verifying your email, you'll finally be able to download your data!

[![](/assets/images/2022/twitch-download.png)](/assets/images/2022/twitch-download.png)

Finally unzip the downloaded file ([how to unzip](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-f6dde0a7-0fec-8294-e1d3-703ed85e7ebc)), and you'll have all your data! You need `_chat_cheer_sub_notif.csv`, `_follow_unfollow.csv`, and `_minutes_watched.csv`.

## Preparing your spreadsheet

### Preparing your twitch analysis sheet
First, open up the [Twitch analysis template spreadsheet](https://docs.google.com/spreadsheets/d/11faLlOZjgjIRu5zCa9KMKONDCnDs1ZpzDy_mozxVjSg/edit). 

Next, click `File` -> `Make a copy` to create an editable version for yourself:

[![](/assets/images/2022/twitch-copy.png)](/assets/images/2022/twitch-copy.png)

### Adding your data

Now you've got an editable copy, we need to import 3 sheets of data to populate all the formulas. Here's the sheets that need importing, followed by the sheet they need to go into:

1. `_chat_cheer_sub_notif.csv` -> `Events`
2. `_follow_unfollow.csv` -> `Follows`
3. `_minutes_watched.csv` -> `Minutes`

On each of these sheets click `File` -> `Import` -> `Upload` tab, and pick your matching `.csv` file. Make sure to change "Import location" for each to "Replace current sheet":

[![](/assets/images/2022/twitch-import.png)](/assets/images/2022/twitch-import.png)

Your data is now in your version of the sheet, there's only 1 step left before it can be analysed!

### Final data tidying

On the "Events" tab, the data needs sorting by type. Click in cell A1, then `Data` -> `Sort sheet` -> `Sort sheet by column A (A - Z)`:

[![](/assets/images/2022/twitch-sort.png)](/assets/images/2022/twitch-sort.png)

In the next section I'll analyse my own data, you can do the same by looking at your own "Totals" sheet.

## Analysing my own data

### Longest sessions

Considering Jerma has been my favourite streamer / YouTuber since... I can remember, I wasn't at all surprised my longest single-sessions were dominated by him! This includes VOD playbacks, so it's likely occasions where I've watched an entire stream in small sessions throughout an afternoon / evening. 426 minutes is just over 7 hours!

The Yogscast streams are probably their yearly Christmas charity livestream event "[Jingle Jam](https://www.jinglejam.co.uk/)".

[![](/assets/images/2022/twitch-longest-session.png)](/assets/images/2022/twitch-longest-session.png)

### Players & streamers

Unfortunately, I couldn't figure out how to sort the players used or streamers watched by frequency, they're just alphabetical! Regardless, the player information likely won't be a surprise, I mostly use the site (`web`), and occasionally Android in a window (`android_pip`), with a little bit of squad streaming (`squad_primary`). 

My top 5 streamers were:
1. Jerma985, 66378 minutes (46 days!)
2. Yogscast, 62538 minutes (43 days!)
3. Hatfilms, 8840 minutes (6.1 days)
4. itswill, 2864 minutes  (2 days)
5. Dafnotdaff 2849 minutes (2 days)

Those Jerma & Yogscast numbers are a little bit terrifying, luckily it's across 5+ years of data!

### Event totals & emotes

I was a little concerned about the number of subscriptions and bit donations that would turn up, but luckily it's only $20 or so! The 160k minutes watched total also implies that Jerma + Yogscast are over 2/3rds of my total minutes watched. 

[![](/assets/images/2022/twitch-event-totals.png)](/assets/images/2022/twitch-event-totals.png)

I don't really talk on Twitch much, so I wasn't surprised I've only Pog'd 54 times. Rookie numbers, eh?

## Calculations

In case anyone is curious, I wanted to run through some of the tricky bits of the `Totals` spreadsheet tab.

**"Player used" and "Streamer watched"**<br>
The 3 columns in these (title, count, minutes) are actually totally independent, with the main challenge coming from the dynamic data (e.g. streamer names) that might be there. I discovered `=SORT(UNIQUE(Minutes!D2:D))` is an easy way to get an alphabetised list of all unique values in a range.

The "Count" column just counts the number of rows in the watch data features this player / streamer, e.g. `COUNTIF(Minutes!$D$2:$D, E5)`. The "Minutes" column works the same, just with `SUMIF`.

One sneaky trick to avoid lots of `0`s in the empty rows is some conditional formatting to set the text colour to white if the value is 0, which *looks* like an empty cell! 

**"Longest sessions"**<br>
This uses a technique I haven't used before. By using `LARGE` we can get the top X value for a range, then find that value again, and fetch another cell in the row. This might seem a convoluted way to fetch a top value but... that's Google Sheets.

**"Streams by year"**<br>
This was my first time messing around with dates in Google Sheets. All we need to do is use `COUNTIF` to count the rows whose timestamp meets both criteria: After or on the 1st Jan in the target year, and before 1st Jan the next year. This is combined with the count / sum logic from the player / streamer section to get totals.

**Chat totals**<br>
Here's where the crazy formulas start! To get the total chat messages (B40), I had to combine 2 bits of data:
1. The total rows in "Events" that are chats or cheers: 
```
COUNTIF(Events!A2:A, "chat") + COUNTIF(Events!A2:A, "cheers")
```
2. The number of times `;` appears in these rows, as the raw data uses this when multiple messages are sent in a session. The number of these present are counted via some borderline magic using `ArrayFormula` and `SUBSTITUTE`:[^chat-messages] 
```
ArrayFormula(SUM(LEN(Events!G2:G))-SUM(LEN(SUBSTITUTE(Events!G2:G,";",""))))
```

[^chat-messages]: [https://www.ablebits.com/office-addins-blog/google-sheets-character-word-count/](https://www.ablebits.com/office-addins-blog/google-sheets-character-word-count/)

**Cheers totals**<br>
The total cheers messages count was easy, just filtering the sheet. My initial approach[^initial-cheers] of finding the total bits was finding all `CheerX` and adding them. This took a *long* time to get working, and I then realised you can send bits using words other than `Cheer` (e.g. `ShowLove100`). Oops!

[^initial-cheers]: [https://stackoverflow.com/q/74103189/608312](https://stackoverflow.com/q/74103189/608312)

My second approach was to just pull out all numbers in "Cheer" messages, and add them together. This has the potential to miscalculate (e.g. "Cheer100 10/10 stream" would count as 120 (100 + 10 + 10)), but it seems pretty accurate. However, this formula is a wild one:
1. At the outer layer, we're using some completely baffling `SUM` and `SPLIT` logic to pull out all numerical values and add them together[^sum-split]. However, this only works for a single cell...
2. Putting a range into this formula works, we just need to dynamically define where the "cheer" rows appear in our Events. We need to do this twice, as the range appears twice in the formula.
3. To get our starting point, we need to count the number of "chat" rows, then add 2: `COUNTIF(Events!$A$2:$A, "chat") + 2)`. This will be the first "cheer" row. 
4. To get our finishing point, we need to use tha same "chat" row count, and add the number of "cheer" rows (plus 1 due to zero indexing). So far, so good.
5. Now the awkward bit. To combine these 2 into a range (e.g. `G100:G120`), we need to use `INDIRECT` (to let us work with the cell reference as a string), and `CONCATENATE` (to combine our starting and ending point into a range).

Here's how the process of building this formula looked, I really hope this makes sense when I try to use it in a few months!
```text
// Sum all numbers
=SUM(SPLIT(A1,CONCATENATE(SPLIT(A1,".0123456789"))))

// Sum all numbers in range
=SUM(SPLIT(A1:A10,CONCATENATE(SPLIT(A1:A10,".0123456789"))))

// Sum all numbers in range, with dynamic starting point
=SUM(SPLIT(A<start point>:A10,CONCATENATE(SPLIT(A<start point>:A10,".0123456789"))))

// Sum all numbers in range, with dynamic starting & ending point
=SUM(SPLIT(A<start point>:A<end point>,CONCATENATE(SPLIT(A<start point>:A<end point>,".0123456789"))))

// Sum all numbers in range, with dynamic starting & ending point, and string mangling
=SUM(SPLIT(CONCATENATE(INDIRECT("A" & <start point> & ":A" & <end point>)),CONCATENATE(SPLIT(CONCATENATE(INDIRECT("A" & <start point> & ":A" & <end point>)),".0123456789"))))

// Sum all numbers in range, with dynamic starting & ending point, and string mangling, and real start / end points, and full cell references
=SUM(SPLIT(CONCATENATE(INDIRECT("Events!G" & (COUNTIF(Events!$A$2:$A, "chat") + 2) & ":G" & (COUNTIF(Events!$A$2:$A, "chat") + COUNTIF(Events!$A$2:$A, "cheer") + 1))),CONCATENATE(SPLIT(CONCATENATE(INDIRECT("Events!G" & (COUNTIF(Events!$A$2:$A, "chat") + 2) & ":G" & (COUNTIF(Events!$A$2:$A, "chat") + COUNTIF(Events!$A$2:$A, "cheer") + 1))),".0123456789"))))
```


[^sum-split]: [https://webapps.stackexchange.com/a/65988/140439](https://webapps.stackexchange.com/a/65988/140439)



## Conclusion

info on what could be done more etc

## References
