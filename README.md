How does this work? (I think) The syntax wildcard and regex-based domain blocks intentionally cause DNS resolution failures for specific Peacock CDN subdomains that deliver ad segments. When the player attempts to request ad manifests or video chunks from those blocked hosts, AdGuard Home returns NXDOMAIN, making the ad-fetch attempt fail instantly. Because Peacock’s playback system is manifest-driven and tolerant to missing ad resources, it simply skips over the failed ad segment requests and continues loading the main content from allowed domains such as play.ovp.peacocktv.com. The end result is that the ads are silently bypassed without breaking playback, since only the ad-serving CDN patterns are null-routed while core playback and manifest delivery remain unaffected.

This repo is updated as often as I can get to it. It's a game of cat and mouse with their servers, but I'm trying my best to minimize and block as many ads as possible. Appreciate all of your testing and feedback!

***Also, check out Reddit user lurking-in-the-bg's Peacock ruleset for a much more condensed and effective version. They've been a huge help with testing and making this project a success!***

https://github.com/lit-bg/Peacock/blob/main/filterlist.txt
