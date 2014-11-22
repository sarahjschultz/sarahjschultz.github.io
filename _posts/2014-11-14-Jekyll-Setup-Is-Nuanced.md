---
layout: post
title: Jekyll Setup Is Nuanced
---

I am running this site through GitHub Pages, because it is pretty simple and plugs into my GitHub account super-smooth like. Configuring it to run at a custom subdomain was less easy, but still not awful.  I learned some things about CNAME records and Apex records, that I did not know before this project — which is major Bonus Town.

Here’s the thing, though. I have been trying to write blog posts about Mistakes I’ve Made, in my learning journey, and have heard great things about Jekyll.

Rolling some of that Jeky swag was not easy.  First, all the docs assume you have nothing in your github.io repo, and that you are starting fresh.  Second, there is this tiny missing step, which proved to be so hidden, that it took 12-hours to uncover.  You must  ```jekyll new```  BEFORE you ```jekyll serve```  — this is essential.
