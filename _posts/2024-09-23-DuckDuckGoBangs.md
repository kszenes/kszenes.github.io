---
layout: post
title: DuckDuckGo Bangs
date: 2024-09-23
description: DuckDuckGo's hidden feature which will turbo-charge your web searching
tags: productivity
# categories: sample-posts
related_posts: false
thumbnail: assets/img/blog/ddg-logo.png
---
# Problem Statement
Nowadays, most of the time when I use a search engine, I usually know on which website I want to arrive on but I don't the exact URL. For instance, if I want to learn more about the 17th century Dutch Tulip Mania, I would usually start by checking out its Wikipedia page. Indeed, I would use "tulip mania wiki" as my search query and click on the first link (corresponding to the Wikipedia page). This process is pretty annoying, especially now that one needs to click through all the cookie menus when using Google as the search engine.
# Solution
{% include video.liquid path="assets/video/blog/ddg-bangs.mp4" class="img-fluid rounded z-depth-1" autoplay=true loop=true controls=true muted=true caption="Example use cases of DuckDuckGo Bangs." %}

Since this is how I use search engines 99% of the time, wouldn't it be nice if I could directly search the website, for instance Wikipedia, for the query, in this case "tulip mania"? One of the coolest native features of DuckDuckGo, a privacy-centric search engine, which is lesser known (at least it was to me) is called DuckDuckGo bangs which enables precisely this. By starting a search query with a bang (an exclamation point) followed by a character code corresponding to the website and then the search query, DuckDuckGo directly issues the query to the website of interest and the user is immediately redirected to the page they were looking for. In our previous example, one would need to use the character code `w` corresponding to Wikipedia:
```text
!w tulip mania
```
## Available Bangs
 {% include figure.liquid loading="eager" path="assets/img/blog/ddg-bangs.png" class="img-fluid rounded z-depth-1" %}

DuckDuckGo bangs supports a huge number of websites (13'567 as of the time of writing this blog post) containing all the major websites as well as many lesser known ones. The list of available bangs can be viewed on their [website](https://duckduckgo.com/bangs) and you can even make a suggestion if a website has not yet been added.
Furthermore, if you simply use a bang followed by your search query without any character code, DuckDuckGo redirects you to the first search result (reminiscent of the "I'm feeling lucky" feature of Google). I use this all the time for lesser known websites that have not been cataloged. In addition, this feature can be used when a bang opens up the search results of the target website to directly jump to the desired page (as in the case of cppreference in the last example).
### Most used bangs
Here are a list of my some of my most used bangs:
- `!`: I'm feeling lucky
- `!w`: Wikipedia
- `!gsc`: Google Scholar
- `!gh`: GitHub
- `!cpp`: Cpp Reference
- `!pypi`: PyPi
- `!g`: Google

## Compatibility with other search engines
Now you might say, this looks cool and all but I don't want to switch my entire search engine to DuckDuckGo because the search results are not as good as Google, with which I would totally agree with. Personally, I use a search engine called StartPage which fetches results from Google without tracking everything you do on the internet. Does this mean you cannot benefit from this cool feature? Far from it, there are a number of plugins for Firefox and Chromium-based web browser plugins which enable you to access this feature while still using your favorite search engine for default queries. The one that I am currently using is [Banger](https://addons.mozilla.org/en-US/firefox/addon/banger/) for Firefox with which I am quite happy. However, there are a number of alternatives that are available by simply searching for "bangs" in the extension store.

### Mobile
On mobile, I use the "Yang! Yet Another Bangs" extension for the android Firefox app.

