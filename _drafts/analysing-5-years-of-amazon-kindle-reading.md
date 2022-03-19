---
title: Analysing 5 years of Amazon Kindle reading (and how you can too!)
author: Jake Lee
layout: post
image: /assets/images/2022/kindle-time-740w.png
tags:
    - Amazon
    - Kindle
    - Books
    - Calculations
    - Data
---

One of my favourite possessions that I spend at least an hour using most days is my Kindle Paperwhite 3 from 2016. I purchased the Paperwhite 5 recently (comparison coming soon!), and decided to analyse the hundreds of books read on my previous Kindle before I say goodbye to it!

In this post I'll talk through a spreadsheet I created to analyse my own Kindle data, and provide details on how you can easily analyse your own.

If you'd just like to see the outcome of the analysis, [here's the Kindle spreadsheet](https://docs.google.com/spreadsheets/d/1eH3KU0Htb_cMmO6-vij0pQBjInj9gX6-5KQACSqBj4s/edit?usp=sharing)!

## Preparing the spreadsheet

### Exporting your Kindle data from Amazon

First, you need to export your purchase history from Amazon. The URL for this varies by country, e.g. [Amazon US](https://www.amazon.com/hz/privacy-central/data-requests/preview.html) and [Amazon UK](https://www.amazon.co.uk/hz/privacy-central/data-requests/preview.html), if you're elsewhere just change the domain to your usual Amazon domain.

You'll then need to select the "Kindle" category, and click Submit Request. It may take a few days to actually receive the download links via email if you use your Kindle a lot, but it'll arrive eventually!

[![](/assets/images/2022/kindle-submit.png)](/assets/images/2022/kindle-submit.png)

### Preparing your data 

When the email eventually arrives, it'll contain a link to download a *lot* of Kindle-related data. For me it had over 50(!) individual pieces of downloadable data, the two we need to download are `Kindle.KindleDocs.zip` and `Kindle.Devices.ReadingSession.zip`.

Unzip both of these downloaded items ([how to unzip](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-f6dde0a7-0fec-8294-e1d3-703ed85e7ebc)), and then make sure you have:
1. Inside `Kindle.KindleDocs/datasets/Kindle.KindleDocs.DocumentMetadata`, a file called `Kindle.KindleDocs.DocumentMetadata.csv` containing all books on your Kindle.
2. Inside `Kindle.Devices.ReadingSession`, a file called `Kindle.Devices.ReadingSession.csv` containing all your Kindle reading sessions.

If they're both there, then you've got all you need!

### Creating the spreadsheet

Head over to [my Kindle analysis spreadsheet](), and click `File` -> `Make a copy`, then save it as whatever you want in your Google Drive:

[![](/assets/images/2022/kindle-copy.png)](/assets/images/2022/kindle-copy.png)

### Importing your data

By default, you'll end up on the "Calculations" spreadsheet. These numbers obviously won't match your data yet, we need to import it!

#### Books

First, we need to import a list of all books in your library:

1. Navigate to the `Kindle.KindleDocs.DocumentMetadata` sheet, click so cell `A1` is selected, then click `File` -> `Import data`.
2. Select your `Kindle.KindleDocs.DocumentData.csv` file you prepared earlier.
3. When importing, **make sure you select "Replace data at selected cell"**! Otherwise, you'll lose some of the book-specific calculations in the spreadsheet.
4. You should have a complete list of all books on your Kindle, along with some equations (columns `L`-`O`) for later! 

| Step 1 | Step 2 | Step 3 | Step 4 |
| -- | -- | -- | -- |
| [![](/assets/images/2022/kindle-import1-thumbnail.png)](/assets/images/2022/kindle-import1.png) | [![](/assets/images/2022/kindle-import2-thumbnail.png)](/assets/images/2022/kindle-import2.png) | [![](/assets/images/2022/kindle-import3-thumbnail.png)](/assets/images/2022/kindle-import3.png) | [![](/assets/images/2022/kindle-import4-thumbnail.png)](/assets/images/2022/kindle-import4.png) |

#### Reading sessions

Now, we need to import all of your Kindle reading session:

1. Go to the `Kindle.Devices.ReadingSession` spreadsheet.
2. Perform the same steps as before, selecting your `Kindle.Devices.ReadingSession.csv` file instead.
3. You should have a very, very long list of all your reading sessions:

[![](/assets/images/2022/kindle-import5-thumbnail.png)](/assets/images/2022/kindle-import5.png)

All done! Going back to the first sheet should now show lots of lovely data analysis! 

## Viewing the spreadsheet

### Per book information

First, on the `...DocumentMetadata` tab, you can see a summary of the reading data grouped by book. The data itself is pretty messy, so only simple calculations are done here. For each book you can see the number of reading "sessions", when the book was first opened, how many milliseconds the sessions lasted for, and the total number of page turn events. 

Using "The Wind in the Willows" as an example, according to the data I read 507 pages, across 82 reading sessions, for a total of 5.5 hours. The book itself is only 200 pages, so whilst the time might be correct (factoring in time with the screen on but not reading), the number of sessions is probably incorrect:

| Title | Sessions | Started | Total ms | Pages turned |
| -- | -- | -- | -- | -- |
| The Wind in the Willows | 82 | 2021-12-18T08:47:52Z | 19898800 (5.5hrs) | 507 |

### Overall data

Heading over to the main `Calculations` sheet, we can see some overall totals:

* Books with valid reading data: 242
* Total reading hours: 1,430.79

This works out to about 50 kindle books and 280 hours of reading between 2017-2022, which sounds about right based on my [Goodreads book history](/analysing-my-goodreads-book-history/).

### Reading by time and year

[![](/assets/images/2022/kindle-time-740w.png)](/assets/images/2022/kindle-time.png)

#### Time of day

### Books read for longest and shortest time

## Extra notes

### Commentary on data

### Sources

        https://www.excel-university.com/how-to-return-a-value-left-of-vlookups-lookup-column/
        https://infoinspired.com/google-docs/spreadsheet/find-the-last-matching-value-in-google-sheets/
        https://www.ablebits.com/office-addins-blog/2017/06/29/countif-google-sheets/

        make sure to link to my goodreads profile & analysis post in a couple of places, and vice versa!