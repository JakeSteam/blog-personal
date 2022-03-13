---
title: Analysing my Google Play purchase history (and how you can too!)
author: Jake Lee
layout: post
image: /assets/images/2022/googleplay-header.png
tags:
    - 'Google Play'
    - Money
    - Calculations
    - Data
---

I've been in the Android ecosystem for a few years now, and tend to make 1-2 Google Play purchases per month, usually removing adverts from a super casual game. To analyse this data, I wrote a little script that is now [hosted on this site](/purchase-history/)!

Whilst there are a few apps already that give you a summary of your purchases, I wanted a solution that could provide basic stats without needing to install anything, connect any services, or transfer any data. 

## Exporting your purchase history

First, we need to download our purchase history from Google Play:

1. Go to [Google Takeout](https://takeout.google.com/settings/takeout).
2. Deselect all preselected options.
3. Tick "Google Play Store".
4. Click "Next step", default settings are fine, then "Create export".

![](/assets/images/2022/googleplay-takeout.png)

Within a couple of minutes, you'll receive an email with a link to download your data export!

![](/assets/images/2022/googleplay-download.png)

## Preparing your purchase history

Once your export is downloaded, unzip it ([unzipping instructions](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-f6dde0a7-0fec-8294-e1d3-703ed85e7ebc), if needed).

Your purchase history will then be a small file at `/Takeout/Google Play Store/Purchase History.json`. 

*Optional: Whilst none of this data is sent during analysis (I don't even have a server to receive it!), you may want to open your export in notepad or another text editor, and redact any sensitive information. For example, you may want to search for "Mastercard" and remove the last 4 digits of your card number.*

## Analysing your purchase history

Finally, we're ready to actually view our data!

Head over to [the purchase history analyser](/purchase-history/), load your file (it isn't uploaded, just loaded locally), and you'll see the following totals:
* Overall amount spent.
* Amount by purchase type (e.g. app, subscription, in-app item).
* Amount by payment method (e.g. Paypal, Google Play balance).
* Amount by year.
* Amount by hour of the day.
* Amount by app.

You're also more than welcome to [look at my purchase history](/purchase-history/?loadsample) if you like, I'll be analysing it below!

## My purchase history

In looking at [my purchase history](/purchase-history/?loadsample), I was a little surprised to see a total amount spent of £450! 

However, the *real* amount spent is closer to £350. This is due to:
* £50 of purchases being made with Google Play credit, earned from [Google Opinion Rewards](https://play.google.com/store/apps/details?id=com.google.android.apps.paidtasks).
* £50 of purchases have been refunded (I accidentally bought something with my phone in my pocket!).

### Items purchased

Unsurprisingly, most of my purchases were in-app purchases, with most apps having 1-2 purchases. Whilst I mostly buy games, I tend to avoid buying shady in-game currencies / boosters and prefer one-off payments for permanent boosts. 

Also unsurprisingly, most of the games are idle games / incrementals! These are quite often aggressively monetised, usually with some sort of permanent XP / reward boost. Once I've spent a few hours with a game, I generally don't mind spending ~£5 on advert removal, especially if it includes additional perks.

### Years purchased

The years I've purchased items makes sense. In 2015 I was first starting to buy apps and in-app purchases, before burning out a bit in 2016. Since then I've been relatively consistent with number of purchases, making a purchase every 2 weeks or so on average, although 2018 was an expensive year!

[![](/assets/images/2022/googleplay-year-thumbnail.png)](/assets/images/2022/googleplay-year.png)

### Times purchased

I was surprised how evenly distributed my purchase times are! I assumed most purchases would be in the early evening, but instead my busiest times seem to be 7-8AM and 11PM! 

In fact, there's at least 1 purchase at every single hour of the day, including the early morning. I think this is due to the occasional night where I have trouble sleeping, and am just killing time on my phone. The sleep deprivation may also lead to a lapse in impulse control..!

[![](/assets/images/2022/googleplay-hour-thumbnail.png)](/assets/images/2022/googleplay-hour.png)
