---
title: "Analysing your Netflix viewing history: How much have you watched, when?"
author: Jake Lee
layout: post
image: /assets/images/2023/
tags:
    - Netflix
    - Analysis
    - Data
---

With Netflix's recent changes to account sharing, I was curious how my (shared!) account had been used over the last 10 years. To do this, I made a spreadsheet, and you can analyse your viewing history easily too!

All of the calculations used in this post [are available in a spreadsheet](https://docs.google.com/spreadsheets/d/1rmQ0BNOr5BrFJQpvTdse7nj_KpFwYDPKW4cmg_3TLXQ/edit?usp=sharing), feel free to look at how the data is calculated. There's also more information [on the formulas](#technical) later on.

Additionally, I've also provided guides previously on how to analyse your data from [Twitch](https://jakelee.co.uk/analysing-my-twitch-data/), [Amazon](https://jakelee.co.uk/analysing-my-amazon-purchases/), [Google Play](https://jakelee.co.uk/analysing-my-google-play-purchase-history/), [YouTube](https://jakelee.co.uk/analysing-my-youtube-subscriptions/), [Kindle](https://jakelee.co.uk/analysing-5-years-of-amazon-kindle-reading/), and [Goodreads](https://jakelee.co.uk/analysing-my-goodreads-book-history/)!

## Getting your data

### Request your data

To get your data, visit [Your Account](https://www.netflix.com/YourAccount) page and navigate to the [Download my personal information](https://www.netflix.com/account/getmyinfo) page.

On here, submit a request, and verify your email. You should receive an email in a day or so (mine took 12 hours) with a link to download.

### Download your data 

Once the email arrives, click the download link, confirm your password, and there'll be a download button:

[![](/assets/images/2023/netflix-download_740w.png)](/assets/images/2023/netflix-download.png)

Finally unzip the downloaded file ([how to unzip](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-f6dde0a7-0fec-8294-e1d3-703ed85e7ebc)), and you'll have all your data! You need the file `netflix-report/CONTENT_INTERACTION/ViewingActivity.csv`.

## Preparing your spreadsheet

### Initial sheet creation

First, open up my [Netflix analysis template spreadsheet](https://docs.google.com/spreadsheets/d/1rmQ0BNOr5BrFJQpvTdse7nj_KpFwYDPKW4cmg_3TLXQ/edit?usp=sharing). 

Next, click `File` -> `Make a copy` to create an editable version for yourself:

[![](/assets/images/2023/netflix-makecopy.png)](/assets/images/2023/netflix-makecopy.png)

### Adding your data

Now you've got a blank spreadsheet, we need to add your data! Navigate to the `ViewingData` sheet, and click `File` -> `Import` -> `Upload` tab, and pick `ViewingActivity.csv`. Make sure to change "Import location" for each to "Replace current sheet":

[![](/assets/images/2023/netflix-import.png)](/assets/images/2023/netflix-import.png)

This might take a few seconds to load, and the analysis sheet will definitely take a few more seconds to run all the formulas for the first time.

**That's it, you're ready to look at your analysis!** In the next section, I'll analyse my data; you can do the same by looking at your own "Analysis" sheet.

[![](/assets/images/2023/netflix-full-thumbnail.png)](/assets/images/2023/netflix-full.png)

## Analysing my own data

### Users

The "User breakdown" table shows Netflix stats split by profile that has watched content. 

I used to watch a *lot* more Netflix, and had exclusive access for the first 3-4 years, so I was pretty surprised I'm only responsible for around 25% of the total watch time! It's still 62 days of watch time, but over 10 years this is to be expected.

Most of the data is very self-explanatory, I was quite interested in seeing my first watch session was almost a decade ago, and that nobody uses the "Kids" profile anymore.

[![](/assets/images/2023/netflix-users-thumbnail.png)](/assets/images/2023/netflix-users.png)

### By time of day / year

The "Hour breakdown" and "Year breakdown" tables show Netflix viewing history split by year and hour of day. Whilst these 2 data sets (and associated graphs) look suspiciously similar, it's a coincidence!

Unsurprisingly my account has watched more and more content over the years, this is more due to my account being shared with more family members than my personal watch time actually increasing.  Time of day distribution is also as expected, I often watch videos as background noise whilst working so I suspect I'll have a smaller "evening" spike than most people.

[![](/assets/images/2023/netflix-time-thumbnail.png)](/assets/images/2023/netflix-time.png)

### By country / device

The "Country breakdown" and "Device breakdown" tables show Netflix viewing history split by countries accessed from, and devices watched on.

Okay okay, this looks a little bit suspicious... I used to have an extension that would load *all* countries' Netflix libraries, hence the occasional trip to Ghana! The non-VPN data is unsurprisingly entirely US & UK based. The device information is much messier than expected. I assumed there'd be some sort of coherent system, but it seems to be all over the place. I recognise my old devices (Galaxy S2, Nexus 7!), makes me weirdly nostalgic!

[![](/assets/images/2023/netflix-countrydevice-thumbnail.png)](/assets/images/2023/netflix-countrydevice.png)

### By content watched

The "Content breakdown" table is a couple of thousand rows long, and lists every single show / film watched on my Netflix account. 

This was by far the hardest part of this spreadsheet to write a formula for, and it's amazing how many awkward TV show names break any code. For example, the show "3%" is formatted as `0.03` and... I've given up fixing it! All other shows / films seem OK, let me know if any others seem broken.

[![](/assets/images/2023/netflix-content-thumbnail.png)](/assets/images/2023/netflix-content.png)

## Technical

### Adding counts to table headers

### Finding unique substrings

### Filter rows by part of timestamp

## Conclusion

words

One last time, [here's the spreadsheet](), and [here's the technical details]()!