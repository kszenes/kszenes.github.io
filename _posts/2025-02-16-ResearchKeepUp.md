---
layout: post
title: Never Miss an Important Publication
date: 2025-02-16
description: How I keep up with all the developments in my field of research
tags: productivity research
# categories: sample-posts
related_posts: false
thumbnail: assets/img/blog/research-overwhelm.png
giscus_comments: true
---

## Introduction

**Keeping up** with the **latest developments** in one's field of research is becoming **increasingly challenging**.
New articles are published daily across numerous journals, and preprint repositories---most notably arXiv---further adding to the overwhelming volume of new information.
**Staying informed**, however, remains **essential**.

In this blog post, I will share **my workflow for staying up to date with the latest publications as they are released**, minimizing the risk of missing important research.
This approach is highly personalized and may not suit everyone, but I hope readers can find valuable insights to incorporate into their own routines.

### 🔔 Google Scholar Alerts

Google Scholar is the go-to resource for searching articles on specific topics, tracking an author's publications, and---if you are so inclined---checking your standing in the academic world through various somewhat questionable impact metrics.

Most researchers are aware that Google Scholar allows users to set up **alerts for new publications** based on **search terms**.
This feature **periodically sends email** notifications with recent papers matching the specified query.
However, keep in mind that Google Scholar scans for the search term anywhere in a publication, not just in the title.
As a result, you may receive a **high volume of loosely related papers** that merely mention the term.
To minimize this noise, I recommend **keeping these alerts limited** to **highly specific search terms**.

Another useful feature is setting up **alerts based on an author's name**.
If an author has a Google Scholar profile, you can easily follow them by clicking the `Follow` button in the top right corner of their profile.

{% include figure.liquid loading="eager" path="assets/img/blog/gscholar-follow-link.png" class="img-fluid rounded z-depth-1" %}
<div class="caption">
    A random aspiring researcher's Google Scholar page
</div>

If a researcher does not have a Google Scholar profile, you can still track their publications by setting up an alert for their name.

However, despite how it appears, following an author does **not always guarantee** that you will receive **updates solely on their work**.
**Publications** from researchers with **identical names** are sometimes **mistakenly included** in the alerts.


#### 📩 Organizing Email Alerts

Once you have set up alerts for key topics and researchers, **your inbox can quickly become cluttered** with notifications from Google Scholar---especially if you have created numerous alerts.
To keep things organized, I **use email filters to automatically categorize** these messages based on custom criteria.

In Gmail, I filter all emails from Google Scholar alerts (identified by the email address `scholaralerts-noreply@google.com`) and move them **out of my inbox into a dedicated label**, in my case `.Google Scholar`.
Since Gmail sorts labels alphabetically, as a personal convention, I prefix all my custom labels with a period (.), which insures that they are grouped together at the top of the `Labels` section in the sidebar menu.


#### ⚠️  Downsides of Google Scholar Alerts

As mentioned earlier, **relying solely on Google Scholar alerts** to stay updated on research developments has its **drawbacks**.
The system presents a trade-off: subscribing to a broad range of queries results in an overwhelming flood of non-relevant publications, while limiting alerts increases the risk of missing important papers.

Google Scholar's alerts are also not always precise with **authors with common names** often being **misattributed**.
Furthermore, since Google Scholar relies on web crawlers to index new publications, there is typically a **delay of several days or even weeks** before a newly released paper appears in search results.

While Google Scholar alerts can be a useful tool, they are best used in combination with other strategies to ensure timely and relevant updates.


### 📖 Tracking New Publications from Specific Journals

A highly effective way to stay updated on research is by **following the latest articles** published in **key journals** relevant to your field.
This method complements the broader search capabilities of Google Scholar and often helps me **discover important papers well before Google Scholar notifies me** of them.


#### 📡 RSS Feeds

While you could manually bookmark your favorite journals and check their homepages every morning, a far more efficient approach is to use **RSS feeds** to gather all this information in one place.

"What are RSS feeds?", you may wonder.
Perhaps, you have come across this logo in the corner of some websites:

<div style="display: flex; justify-content: center;">
    <img src="/assets/img/blog/rss-logo.png" style="max-width: 400px; height: auto;" />
</div>
<div class="caption">
    RSS logo
</div>

RSS (Really Simple Syndication) is a long-standing technology, first introduced in 1999, that **allows websites to distribute content in a standardized, machine-readable format**.
Websites with RSS feeds publish **updates containing headlines, summaries, and links to full articles**.
In fact, RSS is the backbone of podcast distribution as well.

With RSS, you can **stay updated on new publications** without visiting each journal's website individually since **most academic journals provide RSS feeds** for their **latest articles**.
Thankfully, this is also the case for arXiv, where you can subscribe to specific research areas, such as *Chemical Physics* (`physics.chem-ph`).
More information on accessing specific arXiv RSS feeds are detailed [here](https://info.arxiv.org/help/rss.html).

The quality of RSS feeds varies from journal to journal, but most include a **table of contents (TOC) image, article title, abstract, and author list**.
Typically, this information is sufficient to assess whether a paper is relevant to your research.

##### 📲 The Feeder App Reader

There are many RSS reader options available, but I highly recommend the open-source [Feeder](https://github.com/spacecowboy/Feeder) app for Android.
It is **ad-free**, features a **clean UI** with a native dark mode, and offers **extensive customization** options for tailoring the interface to your preferences.

Feeder displays the **TOC image** alongside the article **title**, and selecting an article will (depending on the RSS feed) also show the **author list and abstract**.

<div style="display: flex; justify-content: center;">
    <img src="/assets/img/blog/feeder-example.jpeg" style="max-width: 300px; height: auto;" />
</div>
<div class="caption">
    Example of the Feeder UI for the <em>J. Chem. Theory Comput.</em> journal
</div>

If the article is **open-access**, Feeder can even **fetch the entire article** such that you can read directly from the app.

The app allows you to **group feeds by tags**, making it easy to categorize subscriptions by topic.
You can also **star** articles to save them for later reading.
The app is actively maintained---I personally reached out to the developer with a feature request and received helpful support.

I use Feeder as part of my morning routine to **monitor key journals** as well as my **favorite blogs**---a list of which you can find on my [Resources](/resources) page.


##### 📚 Zotero Integration

As a side note, if you are already using Zotero to manage your research papers, you will be happy to know that it has **built-in RSS support**, making it even easier to track and organize important publications.


## 🔍 Wrapping Up

Staying on top of the latest research can feel overwhelming, but with the right tools and strategies, it becomes much more manageable.
Personally, I have found that **RSS feeds for relevant journals** and **Google Scholar for broad searches** provide complementary approaches for keeping track of the latest publications.
