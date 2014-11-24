---
layout: post
title: Redis As My Sh*t_Store
---

Today I learned about what happens when you have all these fancy methods that depend on your user session, and then all of a sudden the Rails magic stops, and you don't know why.

[Race conditions](http://blog.bottega8.com/when-the-rails-magic-stops-cookies-storage-sessions/)!

Having Redis handle the session information, alleviated the evil, for now.  And this blog post is mostly a way of saving the link to the article at bottega8.