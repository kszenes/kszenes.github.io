---
layout: post
title: DuckDuckGo Bangs
date: 2024-09-23
description: DuckDuckGo's hidden feature which will turbo-charge your web searching
tags: productivity
# categories: sample-posts
related_posts: false
thumbnail: assets/img/blog/ddg-logo.png
giscus_comments: true
---

## Introduction

Nowadays, most of the time when I use a search engine, I usually know on which website I want to arrive at, but I don't know the exact URL. For instance, if I want to learn more about the 17th century Dutch Tulip Mania, I would usually start by checking out its Wikipedia page. Indeed, I would use "tulip mania wiki" as my search query and click on the first link (corresponding to the Wikipedia page). This process is pretty annoying, especially now that one needs to click through all the cookie menus when using Google as the search engine.

## Solution

{% include video.liquid path="assets/video/blog/ddg-bangs.mp4" class="img-fluid rounded z-depth-1" autoplay=true loop=true controls=true muted=true caption="Example use cases of DuckDuckGo Bangs." %}

Since this is how I use search engines 99% of the time, wouldn't it be nice if I could directly search the website, for instance Wikipedia, for the query, in this case "tulip mania"? One of the coolest native features of [DuckDuckGo](https://duckduckgo.com/), a privacy-centric search engine, which is lesser known (at least it was to me) is called DuckDuckGo bangs which enables precisely this. By starting a search query with a bang (an exclamation point) followed by a character code, corresponding to the website, and then the search query, DuckDuckGo directly issues the query to the website of interest and the user is immediately redirected to the page they were looking for. In our previous example, one would need to use the character code `w` corresponding to Wikipedia:

```text
!w tulip mania
```

### Available Bangs

{% include figure.liquid loading="eager" path="assets/img/blog/ddg-bangs.png" class="img-fluid rounded z-depth-1" %}

DuckDuckGo Bangs supports a huge number of websites (13'567 as of the time of writing this blog post) containing all the major websites as well as many lesser known ones. The list of available bangs can be viewed on their [website](https://duckduckgo.com/bangs), and you can even make a suggestion for websites that have not been cataloged yet. Furthermore, if you simply use a bang followed by your search query without any character code, DuckDuckGo redirects you to the first search result (reminiscent of the "I'm feeling lucky" feature of Google). I use this all the time for lesser known websites that do not have their dedicated bang. In addition, this feature can be used when a bang opens up the search results page of the target website (instead of the closest match) to directly jump to the desired page (as in the case of Google Scholar in the last example form the video above).

#### Most used bangs

Here are a some of my most used bangs:

| Bang    | Website           |
| ------- | ----------------- |
| `!`     | I'm feeling lucky |
| `!w`    | Wikipedia         |
| `!gsc`  | Google Scholar    |
| `!gh`   | GitHub            |
| `!cpp`  | Cpp Reference     |
| `!pypi` | PyPi              |
| `!g`    | Google            |

### Compatibility with other search engines

Now you might say, this looks cool and all but I don't want to switch my entire search engine to DuckDuckGo because the search results are not as good as the ones from Google, with which I would totally agree. Personally, I prefer using a search engine called [StartPage](https://www.startpage.com/) which fetches results from Google without tracking everything you do on the internet. Does this mean that you cannot benefit from this cool feature? Far from it. There are a number of plugins for Firefox and Chromium-based web browser plugins which augment your search bar with this feature while still relying on your search engine of choice for default queries. The plugin that I am currently using is [Banger](https://addons.mozilla.org/en-US/firefox/addon/banger/) for Firefox, with which I am quite happy. However, there are a number of alternatives that are available by simply searching for "bangs" in the respective browser's extension store.

#### Mobile

On mobile, I use the [Yang! Yet Another Bangs](https://addons.mozilla.org/en-US/firefox/addon/yang-addon/) extension for the android Firefox app.
