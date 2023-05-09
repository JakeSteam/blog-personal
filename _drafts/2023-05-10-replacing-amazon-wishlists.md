---
title: Amazon wishlists no longer allow items from third party sites, here's the pros and cons of alternative wishlist providers
author: Jake Lee
layout: post
image: /assets/images/2023/
tags:
    - Amazon
---

intro

Here's what the ideal wishlist site would have:

* Ability to easily add new items.
* Able to share the list publicly, ideally with a simple URL.
* No adverts / cost / distracting UI.

## Amazon wishlists

For many years I've had a [public Amazon wishlist](https://www.amazon.co.uk/hz/wishlist/ls/25U6KHU9XCK4B/) that I can share with friends & family before birthdays / Christmas. I add to it throughout the year, and it lets people buy me things I'll *definitely* love.

Whilst Amazon sells a lot of things, about half my list is from third party sites. This might be gift cards for local stores, handmade items from Etsy, or fan merchandise like a Starbase mug. Previously it was possible to add these items to Amazon wishlists with the "Amazon Assistant" extension, however this was disabled in March 2023.

Here's how these non-Amazon items looked, complete with helpful comments:

![](/assets/images/2023/wishlist-amazon.png)

Losing this functionality is a real shame, and [lots](https://www.reddit.com/r/amazonprime/comments/12dy8vh/how_to_add_nonamazon_web_links_to_wish_list/) [of](https://www.reddit.com/r/amazonprime/comments/133131v/is_it_just_me_or_is_it_no_longer_possible_to_add/) [other](https://www.reddit.com/r/AskUK/comments/12dqoy7/alternatives_to_amazon_wishlists/) [customers](https://www.reddit.com/r/amazon/comments/3e3qr3/problems_adding_things_to_wishlist/) miss the functionality too. I can only assume the change is to encourage customers to only purchase Amazon products, or perhaps it was only being kept around as an incentive to use the "Amazon Assistant" extension. Personally this feels a bit of an aggressive move, so I'm moving to an alternative service instead!

Whilst none of these alternatives can perfectly recreate Amazon's ability for strangers to order gifts without knowing my address, hopefully their other benefits make up for this trade-off.

## Notion wishlists

I use Notion extensively at work, and have used it for personal planning before. I [created a basic wishlist](https://jakeleeuk.notion.site/jakeleeuk/Wishlist-97f0850bd047447ea0430ab7d5eba948) and made it public, which is free and works. Notion's main advantage is that it's very easy to use, and has all the formatting and text editing functionality you'd expect.

However, Notion doesn't support custom domains, and it also feels like an unnecessarily complicated web app for just showing a simple list of items in this use case. The design is pretty attractive, but there's a "Try Notion" advert on the screen, and the URL is pretty unappealing: `https://jakeleeuk.notion.site/jakeleeuk/Wishlist-97f0850bd047447ea0430ab7d5eba948`.

Here's how a few items from the wishlist look:

![](/assets/images/2023/wishlist-notion.png)

## GitHub wishlists

So, I've figured out that a plain list of links is good enough for me. Notion was a bit too complex, so what about old reliable Markdown files? 

By editing a [`wishlist.md`](https://github.com/JakeSteam/Notes/blob/main/wishlist.md) file in a brand new [`Notes` GitHub Pages repo](https://github.com/JakeSteam/Notes), I get all the advantages of Markdown and GitHub as well as a simple sharable wishlist: `https://notes.jakelee.co.uk/wishlist.html`.

If you haven't used GitHub Pages before [there's a quickstart guide](https://docs.github.com/en/pages/quickstart), it's definitely the cleanest way to host simple text-based content. The only downside is that there's zero possibility of fancy embeds for items, or any functionality beyond plain text. For me this is OK, but not showing the prices / images definitely makes the buyer's experience worse.

Note that Notion pages can be exported as Markdown via `...` -> `Export`, massively simplifying the transfer.

Here's how the plain text looks on a GitHub Pages site:

![](/assets/images/2023/wishlist-github.png)
