---
parent:
template-type:
template-version:
meeting-date:
title: Measuring Site Responsiveness
layout: post
categories: 
collection_label: post
collection: posts
tags: [post, optimisation]
excerpt_separator: <!--more-->
date: 2024-05-09
date created: Tuesday, May 14th 2024, 4:39:40 pm
date modified: Thursday, May 16th 2024, 10:09:19 am
---

Interaction to Next Paint is a significant new addition to the Core Web Vitals metric family, designed to measure the responsiveness of your web pages.

If you're involved with web technologies, it's an update worth putting on your radar.

It replaced First Input Delay (FID) on March 12, 2024, and there are now less than six months before PageSpeeds Insights, CrUX, and Google Search rankings fully factor it in.

<!--more-->

## What's Different to FID?

In simple terms, FID considers the delay of the first input event and, crucially, can't consider any subsequent interactions.

INP, in contrast, takes into account all of a user's interactions, a broader range of interaction types, and the time it takes for scripts to load after an initial page load.

It provides a rounded view of performance by aggregating a user's interactions with a page and returning the worst-measured score.

## Why Care?

INP has the potential to alter web page optimisation strategies significantly through sites receiving lower PageSpeed Insights scores and impacted search rankings if they don't properly account for the measure.

By looking at your INP score and making changes, you could, for example;

- Improve your User Experience
- Improve your Search Ranking
- Increase site performance
- Reduce any costs associated with bandwidth
- Produce less carbon per visit (see [https://www.websitecarbon.com/](https://www.websitecarbon.com/))

## How Could You Start Measuring?

Use CrUX for a high-level overview of INP, or for straightforward user flows; [DebugBear’s INP Debugger](https://www.debugbear.com/inp-debugger) is a good choice.

When it comes to complex flows, start looking towards Real User Monitoring solutions and be aware of the Chrome team's suggestions for [manually diagnosing slow interactions](https://web.dev/articles/manually-diagnose-slow-interactions-in-the-lab).

**Time to get optimising!**

## References

1. [https://web.dev/articles/inp](https://web.dev/articles/inp)
2. [https://developer.chrome.com/blog/inp-tools-2022/](https://developer.chrome.com/blog/inp-tools-2022/)
3. [https://developer.mozilla.org/en-US/docs/Web/API/PerformanceEventTiming/interactionId](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceEventTiming/interactionId)
4. [https://vercel.com/guides/first-input-delay-vs-interaction-to-next-paint](https://vercel.com/guides/first-input-delay-vs-interaction-to-next-paint)
5. [https://developer.chrome.com/docs/crux](https://developer.chrome.com/docs/crux)
6. [https://pagespeed.web.dev/](https://pagespeed.web.dev/)
7. [https://web.dev/articles/vitals](https://web.dev/articles/vitals)
8. [https://www.debugbear.com/inp-debugger](https://www.debugbear.com/inp-debugger)
9. [https://web.dev/articles/manually-diagnose-slow-interactions-in-the-lab](https://web.dev/articles/manually-diagnose-slow-interactions-in-the-lab)
10. [https://www.websitecarbon.com/](https://www.websitecarbon.com/)
