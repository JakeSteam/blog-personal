---
title: What house can you afford? A calculator to simplify all house buying & selling calculations in the UK
author: Jake Lee
layout: post
image: /assets/images/2023/affordability-banner.png
tags:
    - Finance
    - Spreadsheet
---

Back in February this year, I completed the purchase of a house after owning a flat for a few years. Both of these properties had mortgages, leading to terrifying yet complex calculations that were absolutely crucial yet had no simple explanation! To solve this, I created a spreadsheet with all house-related calculations (e.g. budget), here's an anonymised version. 

Before I share anything, obviously I hold no responsibility for any financial decisions you make, nor am I guaranteeing the spreadsheet is accurate etc, although I did use it without issue for my recent purchase & sale. Please don't sue me for trying to help! I'd also recommend reading [MoneySavingExpert's guide](https://www.moneysavingexpert.com/mortgages/mortgage-fees-stamp-duty/) for lots more info.

Without further ado, here's the spreadsheet with no numbers: <https://docs.google.com/spreadsheets/d/1mRlD0iMLxMsksKXXV1RNfXXr1IHTWiKCNX_EKCO0noA/edit>

And an example with placeholder numbers:

[![](/assets/images/2023/affordability-example.png)](/assets/images/2023/affordability-example.png)

## How to use

### Making a copy

Before you can use the spreadsheet, you need to make your own copy. This will let you edit the figures, download a copy, adjust the calculations, etc.

To do this, just go `File` -> `Make a copy`, then choose where to save it. Easy! 

[![](/assets/images/2023/affordability-copy.png)](/assets/images/2023/affordability-copy.png)

Once you've got a copy, how do you actually make it useful? Simple: Fill in the values, then see what numbers come out!

*Note: Stamp duty rules sometimes change[^changing-rules], so please use a real calculator[^stamp-duty-calc] to double-check this bit.*

[^stamp-duty-calc]: <https://www.stampdutycalculator.org.uk/>
[^changing-rules]: <https://www.gov.uk/stamp-duty-land-tax/residential-property-rates>

### Filling in values 

You should only need to change the new house price, old house price, old house mortgage, and your current savings & income.

Once you've filled those in, the `Mortgage` and `Cash` sections will be populated with the required amounts and your current amounts. I recommend reading the next section for an explanation of each item, but it is optional.

## Explanation / notes

When figuring out all the details of buying and selling property, almost all resources were quite text-heavy guides from companies with vested interests (e.g. moving companies, banks, etc). I really wanted a purely financial / mathematical resource, hence creating my own.

Here's an explanation behind each field:

### Variables

* **New house price**: The listing price of your new house. You likely already know your approximate budget, it's worth changing this number around a bit to see how the figures work out.
* **Old house price** & **Old house mortgage**: The approximate price your current house will sell for. Be conservative, so you can afford to sell for lower than expected! The mortgage should be the amount *remaining*, not the initial mortgage size.
* **Total savings**: The total amount of money (and anybody you're purchasing with) has available. Keep in mind house sales often take a few months, so whilst you'll likely have a bit more than you initially calculate, this will be needed for furniture purchases etc.
* **Total annual income**: Again, this should be combined income. If you have a varying paycheck / are self-employed the rules are different[^self-employed], this spreadsheet is only for predictable salaries.
* **Deposit**: How much of the house price will you be paying as a deposit to the bank? 15% is often recommended as a minimum[^minimum-deposit] (and is what I did), with 20% the average[^average-deposit]. Below that and the loan rates will be painful.
* **Income multiplier**: How much will the bank loan you? This is almost always 4.5x your combined income, but will be lower if you have bad credit, and higher in rare situations. 

[^self-employed]: <https://www.moneysupermarket.com/mortgages/self-employed/>
[^minimum-deposit]: <https://www.themortgagebrain.net/how-much-deposit-do-i-need-to-buy-a-house-in-the-uk/>
[^average-deposit]: <https://www.statista.com/statistics/557891/first-time-buyer-average-deposit-by-region-uk/>

### Buying costs

* **Mortgage fees**: When comparing mortgages, quite a few will add £999 in fees, this is worth factoring in.
* **Stamp duty**: The bands for stamp duty can change, so I recommend double-checking the result with [a real calculator](https://www.stampdutycalculator.org.uk/).

### Selling costs

* **Combined legal fees**: This will be around £1000 per property, so if buying and selling £2000 should be a reasonable estimate.[^conveyancing] 
* **Estate agent fees**: These vary depending on the agent you choose, with 1-2% of sale price being typical[^estate-agent-fees]. You'll have to sign a contract and can sometimes negotiate these numbers down if appropriate. Don't pick the cheapest, pick the best in your area!

[^estate-agent-fees]: <https://www.which.co.uk/money/mortgages-property/home-movers/selling-a-house/estate-agent-fees-and-contracts-aVxAi4F4tdMd>
[^conveyancing]: <https://www.moneysavingexpert.com/mortgages/mortgage-fees-stamp-duty/#conveyancing>

### Totals

* **Mortgage needed** & **Mortgage offered**: The mortgage size you need for your property, and what you are likely to be offered by the bank. If you'll get enough, this will be green!
* **Cash needed** & **Cash owned**: How much cash you'll need for the deposit and all fees, minus the amount you'll get back from selling your current property. Again, if you have enough this will be green.
* **Maximum house price**: The maximum house price you can likely afford. This is approximate, since you'll be limited by cash or mortgage available. Putting this number in as the *New house price* will show if it is actually possible.

## House buying / selling tips

There's a million articles offering tips on buying & selling property (and I read half of them!), so I'll just share a few I found particularly helpful:

* **Use [ReallyMoving](https://reallymoving.com) to find a conveyancer**. I ended up with an excellent one, that made the whole process as easy as possible, let me view all documents / emails on their portal instantly, upload files easily, etc. They also didn't require any chasing, and would actively chase other solicitors!
* **Be in it for the long haul**. It took us almost a year from wanting to buy to actually moving into our house! This was due to our old property taking a while to sell, then taking it off the mortgage briefly as one of us moved to a higher paying job.
* **Be organised and prompt**. When your solicitor asks a question, the entire process is likely waiting for your answer! Reply quickly but always accurately, and make sure you're aware of any upcoming deadlines.
* **Ask questions if you aren't sure**. Your solicitor works for you. If anything doesn't make sense, ask them, they're as interested as you are in everything going smoothly!
* **Monitor house sites closely, and view ASAP**. Houses will often be listed and go under offer within the week, so viewing them as soon as possible is recommended. Set up daily alerts on RightMove, and book a viewing the next day if possible.
* **Be nice to estate agents**. Yes, it can be annoying receiving constant calls from countless estate agents. However, they can tell you about properties days before they go on the public sites, so being clear about your requirements and reliable with answering your phone will help.
* **Accept all viewings**. We struggled to sell our old property, and ultimately had to agree to any viewings. This meant inconvenient times, evenings, weekends, repeat viewings. It can be helpful to find a nearby library / coffee shop where you can work for short periods of time whilst viewings happen.

## Conclusion

Buying a house is stressful, doubly so when buying *and* selling. Having a single place to focus all the calculations made it much easier for me to manage, maybe it will help you too.

I'd really recommend having a read through MSE's [buying a home timeline](https://www.moneysavingexpert.com/mortgages/buying-a-home-timeline/), and [general house buying guide](https://www.moneysavingexpert.com/mortgages/house-buying-guide/). Additionally, [the r/UKPersonalFinance subreddit](https://www.reddit.com/r/UKPersonalFinance/) is an amazing resource, all of your questions probably have detailed answers somewhere on there. 

Good luck!

## References