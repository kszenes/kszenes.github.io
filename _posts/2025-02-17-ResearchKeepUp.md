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

Google Scholar is often the go-to place for searching for articles on a given topic, finding all the publications of a specific author (and estimating your value in society using various somewhat non-indicative impact metrics).
Most people are aware that Google Scholar provides an interface for setting up alerts to new publications based on search terms.
This option periodically sends emails to the user containing recent publications matching the desired query.
Note, however, that Google Scholar identifies this search term not only in the title, but anywhere in a publication which can lead to a lot of noise since many papers might reference a certain technique but not provide anything relevant for the technique developer.
Although I do have alerts for certain---quite specific---search terms, I would suggest limiting them to a small amount in order to mitigate the number of irrelevant suggested articles.

Additionally, there is the option to create alerts for new publications based on the authors name.
If the author has a Google Scholar account, there is a convenient `Follow` button in the top right corner of the researchers profile which automatically sets up the alert.

{% include figure.liquid loading="eager" path="assets/img/blog/gscholar-follow-link.png" class="img-fluid rounded z-depth-1" %}

Note that even though presence of the button on the person's profile suggests that only articles from this author will be alerted, in reality, authors with identical names often get mistakenly included in the email alerts nonetheless.
Publications from scientists that do not have a Google Scholar account can also be tracked by simply setting up an alert for their name.

#### Organizing Emails Alerts

Now that you have set up alerts to all the important topics and people you are interested in, depending on how many alerts you have created, your email might get cluttered with all the alerts from Google Scholar.
In order to better organize them, I rely on filters which automatically categorize emails based on a some custom criteria.
In GMail, I do this by moving all email matching the Google Scholar alert email (`scholaralerts-noreply@google.com`) out of my Inbox and into a dedicated label, called e.g., `.Google Scholar`.
Since GMail sorts labels by alphabetical order, as a convention, I begin the names of all my custom labels with a period, which insures they are grouped together at the top of the `Labels` GMail sidebar.

#### Downsides of Google Scholar Alerts

As alluded to previously, relying exclusively on Google Scholar for getting updates on the research developments can be sub-optimal.
Either one subscribes to a vast array of queries and is inevitably bombarded by irrelevant publications or one limits them and might miss out on an important paper.
Moreover, the search is indiscriminate and even for authors are often missattributed publications.
Lastly, since the Google crawler takes time, usually a couple of days or a weeks, to pick up and catalog new articles, this method will have a slight delay compared to the initial release of the publication.

### 📖 Following Specific Journals

Another strategy for keeping up with research is to follow the latest articles published in the main journals that are relevant for your field.
This approach is quite complementary to the broader search that Google Scholar provides and is usually where I find most of the important articles, well before getting notified of them by Google Scholar.

#### RSS Feeds

While you could simply make a list (or bookmark) your favorite journals and access their homepage one by one as you wake up, a more convenient method is to rely on RSS feeds to gather all this information in a unified way.
What is RSS you might wonder, perhaps you have seen this logo in the corner of some websites:

<div style="display: flex; justify-content: center;">
    <img src="/assets/img/blog/rss-logo.png" style="max-width: 400px; height: auto;" />
</div>
<div class="caption">
    RSS logo
</div>

RSS is an ancient technology, originally developed in 1999, which provides a way to distribute content from websites in a standardized format.
Websites that offer RSS feeds publish updates in a specific, machine-readable format.
This usually includes headlines, summaries, and links to full articles or content.
n addition, RSS is the primary way podcasts are distributed.

So RSS allows the user to get updates from their favorite websites without having to visit each site individually.
Thankfully, most journals provide an RSS feed with all the latest publications as they are released.
This is also the case for common for the arXiv preprint where you can subscribe to a specific topic such as Chemical Physics `physics.chem-ph` (details for accessing arXiv RSS feeds can be found [here](https://info.arxiv.org/help/rss.html)).
The quality of the feed varies from journal to journal, but most provide the reader with the table of contents image, title, abstract and list of authors.
This information is usually sufficient to determine the relevance of the article for the user.

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
