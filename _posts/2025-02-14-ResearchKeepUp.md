---
layout: post
title: Never Miss an Important Publication
date: 2025-02-17
description: How I keep up with all the developments in my field of research
tags: productivity
# categories: sample-posts
related_posts: false
thumbnail: assets/img/blog/research-overwhelm.png
giscus_comments: true
---

## Introduction

Nowadays, it is becoming increasingly difficult to stay up to date with all the developments in one's field of research.
Not only are there numerous journals that publish new articles daily but there are also preprint repositories, the most popular of which is arXiv, which adds to the endless number of new articles
However, it is by no means less important.
In this blog post, I will go over my workflow for getting all the latest publications as they are released and decreasing the chance of me missing any.
As a disclaimer, this workflow is highly opinionated and might not suite everyone but I hope that there might be some useful knowledge to extract for everyone.

### 🔔 Google Scholar Alerts

Google Scholar is often the go to place for searching for articles on a given topic, finding all the publications of a specific author (and determining your value to society using various somewhat non-indicative impact metrics).
Most people are aware that Google Scholar provides an interface for setting up alerts to new publications based on search terms.
This option periodically sends emails to the user containing recent publications matching the query set up by the user.
However, it also pick up the search term anywhere in a publication which can lead to a lot of noise since many papers might reference a certain technique but not provide anything relevant for the technique developer.
While I do have certain quite specific search terms that I have alerts for, I would suggest limiting them to a small amount in order to mitigate the number of irrelevant suggested articles.

On the other side, there is also the option to create alerts for new publications from a specific author.
If the author has a Google Scholar account set up, there is a convenient `Follow` button in the top right corner of the researchers profile which automatically sets up the search alert.

{% include figure.liquid loading="eager" path="assets/img/blog/gscholar-follow-link.png" class="img-fluid rounded z-depth-1" %}

Note that even though presence of the button on the person's profile suggests that only articles from this author will be alerted, in reality, authors with common names often get mistakenly included in the email alerts nonetheless.
Publications from scientists that do not have a Google Scholar account can also be tracked by simply setting up an alert for their name.

#### Organizing Alert Emails

Now that you have set up alerts to all the important topics and people you are interested with, you email might get polluted by these pesky alerts from Google Scholar.
In order to better organize them, you can rely on your email service provider to setup a filter to automatically categorize the email.
In GMail, I do this by moving all email matching the Google Scholar alert email (`scholaralerts-noreply@google.com`) out of my Inbox and into a dedicated lable called e.g., `.Google Scholar`.
Since GMail sorts labels by alphabetical order, as a trick, I start all the names of my custom labels with a period which insures that they appear at the top of the `Labels` column.

#### Downsides of Google Scholar

As alluded to previously, relying exclusively on Google Scholar for getting updates on the research developments can be sub optimal.
Either one subscribes to a vast array of search terms and is bombarded by irrelevant publications or one limits them and might miss out on an important paper.
Moreover, the search is indiscriminate and even for authors can sometimes missattribute publications.
Lastly, since the Google crawler takes time to pick up and catalog new articles, one often only gets notified a couple of days or weeks after the initial release.

### 📖 Following Specific Journals

Another strategy for keeping up with research is to follow the latest articles published in the main journals that are relevant for your field.
This approach is quite complementary to the broader search that Google Scholar provides and is usually where I find most of the important articles.

#### RSS Feeds

While you could simply make a list (or bookmark) your favorite journals and access their homepage one by one as you wake up, a more convenient method is to rely on RSS feeds to gather all this information in a unified way.
RSS feeds are an ancient technology which has stood the test of time and in my opinion is still the best technique for notifying users of updates to a page.
You might not know but this is the technology which podcasts use to notify podcast apps of new episodes.
In the same way, most publishers have a dedicated RSS feed for each individual journal.
This is also the case for preprint servers such as arXiv where you can subscribe to a specific topic such as Chemical Physics `physics.chem-ph`.


<div style="display: flex; justify-content: center;">
    <img src="/assets/img/blog/rss-logo.png" style="max-width: 400px; height: auto;" />
</div>

##### The Feeder App Reader

- RSS feed logo
- Feeder page, contains TOC image, author list and abstract
- This is how I monitor my favorite blogs add link to resources

###### Features

- Open-source
- Group RSS feeds by topic
- Even if RSS feed does not provide it, attempts to fetch the articles (might require cookies). Super helpful developer
- Star favorite article for later read
- Depending on the RSS feed, if the article is open-access it might even fetch the entire article!
