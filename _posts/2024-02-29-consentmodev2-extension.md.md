---
layout: post
title: Wrap up your Consent mode v2 implementation with this GTM-Template
date: 2024-02-29 12:20:00
description: The blog post provides a step-by-step guide for wrapping up your Consent Mode V2 implementation using a GTM template to ensure comprehensive tracking of ad-specific events
tags: Tracking_measurement
categories:
---

**Per march 2024, Consent Mode v2 is mandatory**
It's crucial to ensure that your implementation is up to date. If you're already working on your Consent Mode V2 implementation, here's a GTM template that can help you wrap it up effectively.

**The Challenge with Ad-Specific Tags**
Imagine a scenario where a user clicks on your Google Shopping ad and lands on your website. The 'view_item' event is triggered, but hold on... the consent for ad-specific tags hasn't been granted yet. The result? Your advertising tags, like Facebook's 'view_content', are blocked.

**The GTM Template Solution**
There's a solution to this problem. By implementing a GTM-template, you can reactivate these events as soon as consent for advertising cookies is given. This ensures that you get a more complete picture of product and item list views in your advertising tools.

How to Implement the GTM-template:

1. **Download the Template:** Grab the 'template.tpl' file from [the GitHub repository by mohrstade](https://github.com/mohrstade/backTrack) and upload it to your GTM.
2. **Modify the Script:** We've made a slight modification: at the end of the script, we set 'element.pushType' back to null. This prevents your Google tags from being blocked later in the process.
3. **Trigger the backTrack Tag:** It should be triggered when consent was not yet known and as soon as it gets updated.
4. **Block Google Tags:** All Google tags that use Consent Mode should be blocked if pushType is equal to ‘artificial’.
5. **Testing:** Of course, test whether the script and all tags are working properly.
6. **Configure Tags Early:** Ensure that your configuration tags are triggered as early as possible; they can also be blocked due to lack of consent. Set them up so that they are also triggered on a consent update if it was not previously known.

**The Impact of Small Tweaks**
Small tweaks can make a big difference in your data collection and interpretation. And isn't that what Data & Analytics is all about? Finding smart solutions that make our work more efficient and help us grow.

I'm eager to hear about your experiences! Let's make the world of e-commerce data a bit more comprehensible together.
