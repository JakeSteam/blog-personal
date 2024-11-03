---
title: Analysing 12 years of Amazon purchases (and how you can too!)
image: /assets/images/2022/amazon-header.png
tags:
    - Amazon
    - Money
    - Calculations
    - Data
---

Like many people, I purchase... pretty much everything from Amazon, especially since the pandemic. In this post I'll analyse my own purchasing habits, and provide a template so you can do the same!

All of the calculations used in this post [are available in a spreadsheet](https://docs.google.com/spreadsheets/d/11faLlOZjgjIRu5zCa9KMKONDCnDs1ZpzDy_mozxVjSg/edit), feel free to look at how the data is calculated.

## Getting your data

First, you need to export your purchase history from Amazon. The URL for this varies by country, e.g. [Amazon US](https://www.amazon.com/hz/privacy-central/data-requests/preview.html) and [Amazon UK](https://www.amazon.co.uk/hz/privacy-central/data-requests/preview.html), if you're elsewhere just change the domain to your usual Amazon domain.

Once on data requesting page, select "Your Orders" and submit request:

[![](/assets/images/2022/amazon-request-thumbnail.png)](/assets/images/2022/amazon-request.png)

This will probably take a couple of days to compile, and you'll receive a email when it's done. This email will contain a link to download your data, you want `Retail.OrderHistory.2.zip`:

[![](/assets/images/2022/amazon-download-thumbnail.png)](/assets/images/2022/amazon-download.png)

Finally unzip the downloaded file ([how to unzip](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-f6dde0a7-0fec-8294-e1d3-703ed85e7ebc)), and you'll have your `Retail.OrderHistory.2.csv`! 

## Adding it to the spreadsheet

First, open up the [Amazon analysis template spreadsheet](https://docs.google.com/spreadsheets/d/11faLlOZjgjIRu5zCa9KMKONDCnDs1ZpzDy_mozxVjSg/edit). 

Next, click `File` -> `Make a copy` to create an editable version for yourself:

[![](/assets/images/2022/amazon-copy.png)](/assets/images/2022/amazon-copy.png)

Finally, click `File` -> `Import` -> `Upload` tab, and pick your `Retail.OrderHistory.2.csv`. The default import settings should be fine:

[![](/assets/images/2022/amazon-import.png)](/assets/images/2022/amazon-import.png)

You should now have a very, very big spreadsheet containing all of your data!

[![](/assets/images/2022/amazon-data-thumbnail.png)](/assets/images/2022/amazon-data.png)

In the next section I'll analyse my own data, you can do the same by looking at your own "Calculations" sheet.

## Analysing my own data

Whilst I can't share my own spreadsheet (it contains multiple addresses, payment information, and gift messages), I can share the analysis! One more time, [here's the spreadsheet](https://docs.google.com/spreadsheets/d/11faLlOZjgjIRu5zCa9KMKONDCnDs1ZpzDy_mozxVjSg/edit) if you want to analyse your own purchases.

The total amount spent will SEEM crazy at first glance, but considering I purchase pretty much all household purchases, gifts, cat items, DIY, tech etc from Amazon, it's not too bad.

### Orders by year

Nothing too unexpected here. My Amazon purchasing has steadily creeped up year over year as I've got older, absolutely skyrocketing during the pandemic! The spike in 2016 is due to building a new PC, and buying ~£1000 of parts / accessories.

2022 has obviously barely started, so not many purchases yet.

[![](/assets/images/2022/amazon-byyear.png)](/assets/images/2022/amazon-byyear.png)

### Orders by hour

The shape of this graph surprised me! Whilst I knew I mostly purchased during the evening, I have no idea what I've been buying in the early hours of the morning. 

Not too sure what to make of the dip at 4-5PM, I guess I avoid purchases just before work ends!

[![](/assets/images/2022/amazon-byhour.png)](/assets/images/2022/amazon-byhour.png)

### Orders by method

This reveals the underlying secret, that around 40% of my Amazon purchases aren't actually paid for by me!

I do a few tech interviews / surveys per month, usually giving Amazon vouchers, as well as earning a few larger vouchers from competitions, work, or as gifts. I'm surprised it's SUCH a large percentage though, I guess lots of little gift cards add up.

[![](/assets/images/2022/amazon-method.png)](/assets/images/2022/amazon-method.png)

### Most ordered items

No surprises here for me! My top 3 purchases are an instant coffee I drink daily, and cat food. 

The 4th and 5th most purchased items are fairly cheap headphones (~£10). Before buying my beloved WH-1000XM3s, I would just buy cheap headphones that would break in a few months, hence why I seem to order so many of them! 

[![](/assets/images/2022/amazon-mostordered.png)](/assets/images/2022/amazon-mostordered.png)

## Calculations

In case anyone is curious, I wanted to run through some of the tricky bits of the `Calculations` spreadsheet tab.

* All the `# of orders` and `£ of orders` are just `COUNTIF` and `SUMIF`s for the value to filter by.
* The top 5 product IDs required a bit of SQL, I'm very very grateful to [this StackExchange answer](https://webapps.stackexchange.com/a/127705/140439)!
* Finally, to get the product names once I had the top 5 product IDs, I had to use [`VLOOKUP`](https://support.google.com/docs/answer/3093318?hl=en-GB). Very odd results were being returned initially, until I figured out I need to set `is_sorted` to false. It's `true` by default, but Google recommend setting it to false! 

## Conclusion

Whilst I would have liked to gather proper data for each product (e.g. category, rating, etc), this would have been a far, far more complex undertaking. This simple analysis still provides some interesting insights, and can easily be expanded on. It's also kinda fun playing around with spreadsheets, and seeing what is possible!
