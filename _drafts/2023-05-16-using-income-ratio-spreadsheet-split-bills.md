---
title: Using an income ratio spreadsheet & Splitwise to split household expenses fairly and transparently as a couple
author: Jake Lee
layout: post
image: /assets/images/2023/ratio-example.png
tags:
    - Finance
    - Relationships
---

Every couple I know has a different way of splitting their household finances, with the goal of making both sides contribute enough whilst also having financial independence. My partner and I use a method that handles bill increases, pay rises, and day to day purchases easily and fairly despite different incomes. Here's an explanation and template, to save you trial and error!

[Here's the example spreadsheet (with fake values)](https://docs.google.com/spreadsheets/d/12Y-qo7uVEvAMLfDzJvbHf4MDrCDiUHGnC4XkhPq5vLY/edit?usp=sharing), it looks like this:

[![](/assets/images/2023/ratio-example_thumbnail.png)](/assets/images/2023/ratio-example.png)

## Context

### Requirements

My partner and I both work full-time for roughly similar incomes, and have our own outgoings (hobbies, clothes, books, etc). We don't want to be paying for each other's personal interests, but we do want to be paying for things we both use. However, I earn slightly more than my partner, so should of course pay more of the bills, whilst also having a bit more "personal" money to make up for it.

As a full disclaimer we have been lucky career-wise over the last few years, and do have some disposable income. If bills are barely being made each month this approach may not work, or might require tweaks.

### Accounts

A lot of people use shared accounts, and this approach absolutely can work for that. As I tend to be a lot more ~~obsessive~~ organised with money, payments almost always come out of my account, then my partner just transfers the total amount across each month. 

My partner's name is still on these bills (e.g. council tax, our mortgage), it just comes from my account. However, there's no reason the approach described in this article can't be used to calculate the amount required in a shared account each month.

## Solution

So what's the actual approach?

Well, we have 2 types of expenses, fixed and variable. For fixed expenses they are planned out in a spreadsheet, for variable expenses they get added to Splitwise and "settled up" at the end of the month.

These expenses are then paid according to the ratio of post-tax income you both earn.

### Ratio

When working out what each partner needs to pay, using their monthly income is a great starting point. If someone earns £500 a month and something else earns £1000, the second person should pay twice as much! However, make sure to use the **post-tax** income, as this can differ drastically at higher incomes due to progressive taxes.

Once the ratio between both people is calculated, all expenses can be split according to this ratio. Using our 500:1000 ratio from before gives us 1:2, which means for a £300 bill the cost will be split £100:£200. 

This isn't a complicated formula by any means, but the clever bit is storing all these values in a spreadsheet avoiding any of the dull calculations. Additionally, real world values are rarely this simple, and splitting a £23.50 bill between people earning £1334 and £1766 per month is pretty horrible without a calculator!

Here's a simplified version of [the spreadsheet](https://docs.google.com/spreadsheets/d/12Y-qo7uVEvAMLfDzJvbHf4MDrCDiUHGnC4XkhPq5vLY/edit#gid=0) to help show what's going on:

#### Incomes

| Value | Total (P1 & P2) | Person 1 | Person 2 |
| --- | --- | --- | --- |
| Income | £1300 | £800 | £500 |
| Income post-tax | £1000 | £600 | £400 |
| Percentage | 100% | 60% | 40% |

In this scenario, Person 1 will pay 60% of all bills, and Person 2 40%.

#### Expenses

| Bill | Total (P1 & P2) | Person 1 | Person 2 |
| --- | --- | --- | --- |
| Mortgage | 500 | 300 | 200 |
| Electricity | 100 | 60 | 40 |
| Water | 80 | 48 | 32 |

Using Mortgage as an example, we divide the total by the total percentage, then multiply by each person's contribution. For example `(500 / 100) * 60 = 300`. 

### Fixed expenses

Realistically most expenses are known in advance. You know your mortgage payment, your energy bill, your insurance costs. Work out the monthly direct debit amounts, put them [into a copy of the spreadsheet](https://docs.google.com/spreadsheets/d/12Y-qo7uVEvAMLfDzJvbHf4MDrCDiUHGnC4XkhPq5vLY/edit#gid=0) (see [Making your own](#making-your-own)), and you should end up with an accurate monthly payment for both people involved!

The bold, outlined number below indicates what each person needs to pay, and the number below shows their leftover money each month:

[![](/assets/images/2023/ratio-totals.png)](/assets/images/2023/ratio-totals.png)

### Variable expenses

Things like day to day shopping or DIY equipment can't be predicted, so we instead log these in a cost splitting app [Splitwise](https://www.splitwise.com/).

The free plan is plenty for us, and whilst you can add receipts / details, in a relationship there's hopefully enough trust that just adding the name of the shop is enough!

We also use Splitwise for specific expense tracking, such as hotels / flights / bookings for a holiday.

[![](/assets/images/2023/ratio-splitwise_thumbnail.png)](/assets/images/2023/ratio-splitwise.png) <br>*<sup>Promotional image from [Splitwise.com](https://www.splitwise.com/)</sup>*

## Making your own

So, how can you make your own ratio-based expenses spreadsheet?

1. Open [the example spreadsheet](https://docs.google.com/spreadsheets/d/12Y-qo7uVEvAMLfDzJvbHf4MDrCDiUHGnC4XkhPq5vLY/edit#gid=0).
2. Go `File` -> `Make a copy`, save the copy.
3. Edit the following fields:
    1. **Income** (D2/3, E2/3)
    2. **Expenses** (D6-16+ / E6-16+), duplicating and grouping rows as needed.

Simple!

## Conclusion

One of my favourite parts of this setup is how pay rises are handled. When one person starts earning more, they obviously have more spending money, but their bill payments also increase a bit, ensuring the other person pays a bit less. It's as if both people get a pay rise, but the responsible party gets a higher one!

Additionally, it's up to you to decide how inclusive this expenses management is. For example, we choose to exclude any bonus income and personal expenses.

Don't forget you can also add notes on Google Sheets, I find it helpful to add small notes to expenses like insurance, to remember renewal date / policy provider.

