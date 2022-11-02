---
title: How do you use Twitch? A guide to analysing your emotes, subscriptions, chat messages, and viewing history!
author: Jake Lee
layout: post
image: /assets/images/2022/twitch-header.png
tags:
    - Twitch
    - Calculations
    - Data
---

Along with [YouTube](/analysing-my-youtube-subscriptions/), I also watch quite a lot of Twitch streams & VODs. In this post, I'll share my spreadsheet for analysing my top streamers, chat messages, playback methods etc using my data export, along with instructions for you to do the same! 

All of the calculations used in this post [are available in a spreadsheet](https://docs.google.com/spreadsheets/d/16bE6egEtML9t6rPVaqtLMZU7pPjixSlmG_JhVQ0dJkY/edit?usp=sharing), feel free to look at how the data is calculated. There is also a [separate technical write-up](https://blog.jakelee.co.uk/6-useful-google-sheets-techniques) with more detail on all the formulas.

## Getting your data

First things first, there might be a multi-month delay here. There was an astonishing *6 month delay* between my data request and actually receiving my data!

### Request your data

There's unfortunately no easy way to automatically export your data from Twitch, so you'll have to [fill in their Data Access Request Form](https://www.twitch.tv/p/en/legal/privacy-choices/#:~:text=hold%20about%20you%2C-,submit%20your%20request%20here.,-You%20will%20need) (linked from [Privacy Choices](https://www.twitch.tv/p/en/legal/privacy-choices/)), providing verification that you own the account you are requesting data from.

| Request & response | Request |
| --- | --- |
| [![](/assets/images/2022/twitch-request-thumbnail.png)](/assets/images/2022/twitch-request.png) | Hey,<br><br>I'd like to export as much of my Twitch account data as possible please. Ideally this would include:<br>- Chat messages sent<br>- Viewtime per channel (live + VOD)<br>- Channel subscription history<br>- Any other user data you have immediately available<br><br>Thank you very much! |

### Download your data 

When your data is finally ready, you will receive an email titled "Your Privacy Request Needs Attention". After following the link and verifying your email, you'll finally be able to download your data.

[![](/assets/images/2022/twitch-download.png)](/assets/images/2022/twitch-download.png)

Finally unzip the downloaded file ([how to unzip](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-f6dde0a7-0fec-8294-e1d3-703ed85e7ebc)), and you'll have all your data! You need `_chat_cheer_sub_notif.csv`, `_follow_unfollow.csv`, and `_minutes_watched.csv`.

## Preparing your spreadsheet

### Initial sheet creation
First, open up my [Twitch analysis template spreadsheet](https://docs.google.com/spreadsheets/d/11faLlOZjgjIRu5zCa9KMKONDCnDs1ZpzDy_mozxVjSg/edit). 

Next, click `File` -> `Make a copy` to create an editable version for yourself:

[![](/assets/images/2022/twitch-copy.png)](/assets/images/2022/twitch-copy.png)

### Adding your data

Now you've got an editable copy, we need to import 3 sheets of data to populate all the formulas. Here's the files that need importing, followed by the sheet they need to go into:

1. `_chat_cheer_sub_notif.csv` -> `Events`
2. `_follow_unfollow.csv` -> `Follows`
3. `_minutes_watched.csv` -> `Minutes`

On each of these sheets click `File` -> `Import` -> `Upload` tab, and pick your matching `.csv` file. Make sure to change "Import location" for each to "Replace current sheet":

[![](/assets/images/2022/twitch-import.png)](/assets/images/2022/twitch-import.png)

Your data is now in your version of the sheet, there's only 1 step left before it can be analysed!

### Final data tidying

On the "Events" tab, the data needs sorting by type. Click in cell A1, then `Data` -> `Sort sheet` -> `Sort sheet by column A (A - Z)`:

[![](/assets/images/2022/twitch-sort.png)](/assets/images/2022/twitch-sort.png)

**That's it, you're ready to look at your analysis!** In the next section, I'll analyse my data; you can do the same by looking at your own "Totals" sheet.

## Analysing my own data

### Longest sessions

Considering Jerma has been my favourite streamer / YouTuber since... I can remember, I wasn't at all surprised my longest single sessions were dominated by him. This includes VOD playbacks, so it's likely occasions where I've watched an entire stream in small sessions throughout an afternoon / evening. 426 minutes is just over 7 hours!

The Yogscast streams are probably me catching up on their yearly Christmas charity livestream event "[Jingle Jam](https://www.jinglejam.co.uk/)".

[![](/assets/images/2022/twitch-longest-session.png)](/assets/images/2022/twitch-longest-session.png)

### Players & streamers

Unfortunately, I couldn't figure out how to sort the players used or streamers watched by frequency, they're just alphabetical. Regardless, the player information likely won't be a surprise, I mostly use the site (`web`), and occasionally Android in a window (`android_pip`), with a little bit of squad streaming (`squad_primary`). 

My top 5 streamers were:
1. Jerma985, 66378 minutes (46 days!)
2. Yogscast, 62538 minutes (43 days!)
3. Hatfilms, 8840 minutes (6.1 days)
4. itswill, 2864 minutes  (2 days)
5. Dafnotdaff 2849 minutes (2 days)

Those Jerma & Yogscast numbers are a little bit terrifying, luckily it's across 5+ years of data!

### Event totals & emotes

I was a little concerned about the number of subscriptions and bit donations that would turn up, but luckily it's only $20 or so. The 160k minutes watched total also implies that Jerma + Yogscast are over 2/3rds of my total minutes watched. 

[![](/assets/images/2022/twitch-event-totals.png)](/assets/images/2022/twitch-event-totals.png)

I don't really talk on Twitch much, so I wasn't surprised I've only Pog'd 54 times. Rookie numbers, eh?

## Conclusion

Overall, I'm fairly happy with this analysis. It answers most of the initial questions I initially had (who do I watch most, how often do I chat etc), although in not quite as much detail as I'd like. If the streamer list and player list could be ordered by frequency not alphabetically, the results would be much easier to parse.

Additionally, the 6 month delay to get my data from Twitch was ridiculous. Other services take a week or so, and this 6 month delay means all my recent data is not included. I'm not sure if this was a technical delay (e.g. waiting for data to enter long term storage) or just a very backlogged system, but it seemed excessive.

I'm also happy with the sheer amount of new data analysis techniques I've learnt throughout this process, even if some of them are very verbose! I still struggle quite a bit with Google Sheets' data structures, and whenever I want to analyse more than a single cell I always have to look up a guide. 

One last time, [here's the spreadsheet](https://docs.google.com/spreadsheets/d/16bE6egEtML9t6rPVaqtLMZU7pPjixSlmG_JhVQ0dJkY/edit?usp=sharing), and [here's the technical details](https://blog.jakelee.co.uk/6-useful-google-sheets-techniques)!