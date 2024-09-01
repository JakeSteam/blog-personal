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

## Conclusion

Well, Jekyll ultimately is just a series of simple steps! However, the implementation of plugins, converters, and styling seems to have been very intentionally designed for extensibility, making users' lives as easy possible. Nice.

[^jekyll-rendering]: <https://jekyllrb.com/docs/rendering-process/>
[^jekyll-generators]: <https://jekyllrb.com/docs/plugins/generators/>
[^jekyll-converters]: <https://jekyllrb.com/docs/plugins/converters/>
[^jekyll-liquid]: <https://shopify.github.io/liquid/>
[^jekyll-watch]: <https://github.com/jekyll/jekyll-watch>
[^jekyll-watch-rb]: <https://github.com/jekyll/jekyll-watch/blob/master/lib/jekyll/watcher.rb>
[^jekyll-philosophy]: <https://jekyllrb.com/philosophy/>

## 2: Cloudflare pages

## 3: Muscle building diet

## 4: F1 aero

## Day 5:

## Day 6:

## Day 7:

## Day 8:

## Day 9:

## Day 10:

## References
