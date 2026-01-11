---
tags:
  - note
  - university
subject: "[[it2030]]"
chapter: 1
unit: 2
title: Script
---
# Presentation Script

## Introduction
- Hello everyone, my name is Chu Quang Lượng. Today I want to tell you about...
(ad show).
- Oh, it seems we have some technical issues here, let me fix it real quick.
(closes ad)
- Okay. So you see, advertisement, or ads, are annoying, right? They distract you from the site's content, redirect you to other websites. Some ads even track user's behaviour. [^1]
- But what if I told you, there's a piece of technology that can get rid of all the advertisement you see on website? Introducing... ad blockers.

## What's ad blockers? How do they work?
- Ad blocker is any piece of software that automatically hide/block advertisement from showing on websites or applications. The most common form of ad blocker is through browser extensions such as AdBlock, uBlock Origin,etc...
- So, how do ad blockers work? When you access a website, the web browser make HTTP requests to the web servers that host the website. The web servers usually will return the website's content to the web browser for display. The content contains HTML files, which describe the raw content, CSS stylesheet, which is used to make the site prettier and JavaScript scripts, which helps for user interaction.
- To load ads in website's content, the web browser will make requests to ads server. This is where our ad blockers come into play. Ad blocker use a list that contains several rules that identify which URLs point to an ad server, and block requests to them. [^2]
- Sometimes ads can be sneakily shown without triggering a HTTP request by encode images in base64. Ad blockers also contain a list of CSS element selector that find ad element and hide them.

## Benefits of ad blockers
- Ad blockers help reduce distractions on the web, helps user to focus on the site's content. Ad blockers also help increase user's engagement and activiy on the site. [^3]
- Ad blockers can reduce traffic to site, improving site's performance and reducing device's power usage. [^4]

## Response from websites
- Despite having many benefits for user, ad blockers will reduce websites revenue through ad. According to a report, in 2024, ad blocking solution cost publishers $54 billion in lost ad revenue [^5]. So it's natural for website owner to implement anti ad-blocker features.
- One of the ways these features are implemented is through blocking content if an ad-blocker is detected. A pop up might appear to ask you to disable or whitelist the current site to maintain access to site's content.

## Solutions/Alternatives
- While using ad-blockers provides many benefits, you should consider whitelisting some sites to support the site's owner. Some platform also provide ad-free subscription to their services.
- If you're a website owner/creator, you also have a lot of options to recover from ad-blocking revenue lost. You can embed ads directly in your content, which might not be detected by ad-blocker. Making ads less disruptive and more "better looking" can also persuade user to disable ad-block on your site.

## Conclusion
- In this presentation, I've show you how ad blockers work, the benefits, drawbacks of ad blockers and some tips for both users and creators. Hope this help you to use the Internet safer, easier, and less annoying. Thank you for listening.
## References
[^1]: [Personalized advertising - Advertising Policies Help](https://support.google.com/adspolicy/answer/143465?hl=en)
[^2]: [How does AdBlock work? – AdBlock](https://helpcenter.getadblock.com/hc/en-us/articles/9738502775315-How-does-AdBlock-work#:~:text=AdBlock%2C%20like%20all%20ad%20blockers,in%20languages%20other%20than%20English.)
[^3]: [The Effect of Ad Blocking on User Engagement with the Web \| Proceedings of the 2018 World Wide Web Conference](https://dl.acm.org/doi/10.1145/3178876.3186162)
[^4]: [Impact of Ad Blockers on Computer Power Consumption while Web Browsing: A Comparative Analysis \| European Journal of Electrical Engineering and Computer Science](https://www.ejece.org/index.php/ejece/article/view/650#:~:text=The%20findings%20indicate%20substantial%20differences,environmental%20impact%20of%20online%20activities.)
[^5]: [Ad Blocker Usage and Demographic Statistics in 2024](https://backlinko.com/ad-blockers-users)