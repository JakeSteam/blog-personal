---
title: "An educational September: Days 1-10"
author: Jake Lee
layout: post
image: /assets/images/2024/
tags:
  - Education
  - Hobby
maxheader: 2
---

intro

## 1: Jekyll build process

- **What do I want to learn?** How does Jekyll convert my list of posts and templates into... an actual site? Is it just convert markdown, glue it together, and done?
- **How much do I know already?** Despite making a theme used on various sites... not much! I know how to use it, and how to customise it, but not about how it actually compiles, how the automatic rebuilding works, or anything else.

### Building

Luckily, Jekyll has an entire page[^jekyll-rendering] dedicated to how the build process works! The build process is just a series of steps running in order, as you'd expect, some with substages:

1. **Setting up plugins** (e.g. initialising).
2. **Reading source files**.
3. **Running generators[^jekyll-generators]**: Generate dynamic variables / content based on site contents, e.g. pages for article categories, or a sitemap, or an RSS feed.
4. **Rendering templates** (each substage is optional, depending on file extension, front matter, and content):
   1. Interpreting the "Liquid"[^jekyll-liquid] code.
   2. Running converters (e.g. Markdown -> HTML, SASS -> CSS)[^jekyll-converters].
   3. Populating layouts (e.g. putting a post's content into the `post.html` template).
5. **Saving generated files**.

### Other

- **Incremental regeneration**: Jekyll's documentation has a dedicated page for incremental regeneration, and it works how you might guess: By keeping track of last modified dates (and which files feed into which others) in a `.jekyll-metadata` file. Simple. However, I don't actually use this, I use...
- **Watch**: Enabled by default, and no new release in 5 years(!)[^jekyll-watch]. Whilst I had intended to learn how this actually works, it's just a short Ruby script[^jekyll-watch-rb] so not much to look at.

Interestingly, the very first item on Jekyll's "Philosophy" page[^jekyll-philosophy] is "No Magic", with the explicit intention of users (e.g. me) being able to figure out how it works. Convenient!

> Jekyll is not magic. A user should be able to understand the underlying processes that make up the Jekyll build without much reading.

Perhaps this shouldn't have been a surprise, since I've regularly added plenty of new features to my [minimaJake theme](https://minima.jakelee.co.uk/) and things just... kinda make sense? I can copy the existing template, copy existing plugins, all because the project aims for simplicity and obviousness.

### Conclusion

Well, Jekyll ultimately is just a series of simple steps! However, the implementation of plugins, converters, and styling seems to have been very intentionally designed for extensibility, making users' lives as easy possible. Nice.

[^jekyll-rendering]: <https://jekyllrb.com/docs/rendering-process/>
[^jekyll-generators]: <https://jekyllrb.com/docs/plugins/generators/>
[^jekyll-converters]: <https://jekyllrb.com/docs/plugins/converters/>
[^jekyll-liquid]: <https://shopify.github.io/liquid/>
[^jekyll-watch]: <https://github.com/jekyll/jekyll-watch>
[^jekyll-watch-rb]: <https://github.com/jekyll/jekyll-watch/blob/master/lib/jekyll/watcher.rb>
[^jekyll-philosophy]: <https://jekyllrb.com/philosophy/>

## 2: Fruit tree growing

- **What do I want to learn?** I have a few small fruit trees in my garden, and they're doing whatever they want. Should I be helping them somehow? Pruning them?
- **How much do I know already?** Essentially nothing. I remove any dead fruits, and sometimes trim the trees if they're reaching too far towards each other, but I don't know if this is correct.

### Notes

- They need a lot of watering[^fruits-watering]! I haven't been giving them any besides what they occasionally catch when I water the lawn (not at all this year).
- Similarly, I should make sure they get some bonus nutritious garden compost[^fruits-compost], or the chicken manure pellets I found in my garage!
- I should also sometimes clear some space around the bottom, so they get the compost nutrients not the grass they're growing in.
- "Thinning" is a thing! By getting rid of some fruit in May-ish when they've just started appearing, the tree can put all its energy into fewer, bigger fruits.
- Maintenance of the tree's shape seems pretty flexible. Prune in winter if you want MORE tree, prune in spring & summer if you want to keep it about the same size[^fruits-pruning]. I'll do the latter.

### Conclusion

I need to look after my trees better! Next spring I'm looking forward to thinning out the fruit, and pruning the trees so they're a less chaotic shape. Hopefully it'll help provide more plums and apples to eat, I definitely noticed having fewer this year than the one before.

However, it really isn't that complicated. Like with seemingly everything else in the garden, it just needs a bit of effort at the right time. If only I was retired and could do a little gardening daily..!

[^fruits-watering]: <https://www.ashridgetrees.co.uk/advice/essential-aftercare#:~:text=All%20fruit%20trees%20need%20a%20steady%2C%20consistent%20even%20supply%20of%20moisture.>
[^fruits-compost]: <https://www.rhs.org.uk/fruit/fruit-trees/feeding-and-mulching>
[^fruits-pruning]: <https://www.woodlandtrust.org.uk/blog/2018/02/when-to-prune-fruit-trees/>

## 3: 80s F1 drivers?

Okay, this doesn't really count, I had a busy day!

I spent a couple of hours reading [Nigel Mansell's autobiography](https://www.goodreads.com/book/show/5721352-driven-to-win) from just _before_ he won the F1 world championship!

It was pretty interesting reading him talk about many now-legends of the sport as current drivers, and how significantly reliability factored into performance in those days. Since I'm [still a newcomer to F1](https://jakelee.co.uk/why-i-fell-in-love-with-formula-1/), I always enjoy reading of accounts from before I was watching.

## 4: Cloudflare pages

## 5: Muscle building diet

## 6: F1 aero

## Day 6:

## Day 7:

## Day 8:

## Day 9:

## Day 10:

## References
