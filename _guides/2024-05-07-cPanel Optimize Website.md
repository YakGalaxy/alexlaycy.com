---
title: cPanel Optimize Website
layout: post
categories:
collection_label: guide
collection: guides
tags:
  - guide
  - optimisation
excerpt_separator: <!--more-->
date: 2024-05-07
comments: false
---


![overview image of a cPanel](\assets\cPanel - Overview.webp)

Via [https://hostandtech.com/help/whm-cpanel/how-to-optimize-website-using-cpanel-optimize-tool/](https://hostandtech.com/help/whm-cpanel/how-to-optimize-website-using-cpanel-optimize-tool/)

A _significant_ number of hosting providers use [cPanel](https://www.cpanel.net/), a _“server and site management platform”_ with a wide range of built-in utilities and software installation scripts.

There’s a common misconception that using cPanel implies a lack of seriousness or professionalism in website creation or hosting. This is a fallacy. It’s important not to dismiss widely used tools, even if you perceive them to have limitations. They are popular for a reason.

Anyway, back to cPanel…

<!--more-->

One of the most intriguing utilities within cPanel is the **‘**[**Optimize Website**](https://docs.cpanel.net/cpanel/software/optimize-website/)**’.** It’s not just an ‘easy win’ (though I dislike the term) but **_a potentially powerful_** tool that simplifies the configuration of [Apache’s mod_deflate module](https://httpd.apache.org/docs/current/mod/mod_deflate.html), enhancing your website’s performance through compression.

**In simple terms**, this Apache module _“allows output from your server to be compressed before being sent to the client over the network.”_

Avoid compressing files that are either already compressed or where quality will be impacted with less control than you’d like, and you could see a decrease in file size of [up to 43%](https://www.linuxjournal.com/article/6802).

While protocols such as HTTP/2 and HTTP/3 offer built-in compression mechanisms, many sites still rely on HTTP/1.1 OR have content that would benefit from being compressed on the server side.

# Choosing MIME Types

**Focus on Text-Based Content:** Text-based files benefit the most from compression (and aren’t already compressed). They typically compress well, which could significantly improve load times. This not only improves your site’s performance but also reduces bandwidth usage.

**Exclude Binary Files:** These are usually already compressed in their formats.

**Consider Modern Formats:** Include MIME types corresponding to modern web development practices, such as newer JavaScript modules and data interchange formats.

**Exclude Dynamically Generated Files:** Files that are dynamically generated and already compressed by the server (like some JSON APIs) might not benefit from additional compression. They could even add unnecessary CPU load.

**Server Capabilities:** Ensure your server’s configuration and capabilities can handle the compression workload without causing performance bottlenecks.

# MIME Types: A Foundation List

⚠️ Adjust or add to this list based on your individual configuration.

- text/html — HTML documents.
- text/css — CSS files.
- application/javascript — Standard MIME type for JavaScript files.
- text/plain — Plain text files.
- text/xml — XML files.
- application/xml — Generally used for XML files in applications.
- application/json — JSON format.
- text/csv — Comma-separated values files.
- application/xhtml+xml — XHTML documents.
- application/x-httpd-php — PHP files, if they are outputting HTML that isn’t dynamically compressed.
- text/markdown — Markdown files, typically used in static site generators.
- application/ecmascript — Enhanced version of JavaScript.
- text/javascript — Legacy MIME type for JavaScript (consider including if older scripts are used).
- application/x-javascript — Another JavaScript MIME type, less commonly used but included for completeness.

# Testing

As a quick test, you can input a URL at [https://http.dev/compression/test](https://http.dev/compression/test) to see if end-to-end compression is being utilised, and which type.

# References

- [MDN — Common MIME Types](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types/Common_types)
- [cPanel Docs — Optimize Website](https://docs.cpanel.net/cpanel/software/optimize-website/)
- [Linux Journal — Compressing Web Content with mod_gzip and mod_deflate](https://www.linuxjournal.com/article/6802)

# Download the CheatSheet

- [Introduction ⇱](https://www.alexlaycy.com/assets/cPanel%20-%20Optimize%20Website%20-%20Quick%20Sheet%20-%20Introduction.png)
- [Foundation List ⇱](https://www.alexlaycy.com/assets/cPanel%20-%20Optimize%20Website%20-%20Quick%20Sheet%20-%20Foundation%20List.png)