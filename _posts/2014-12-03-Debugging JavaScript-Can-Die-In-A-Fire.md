---
layout: post
title: Debugging JavaScript Can Die in a Fire
---

Debugging parse errors in JS is literally the worst. I've done some searching, and I've not found any particularly well-established techniques for effectively flushing out your JS bugs, aside from the super-annoying, "When you have enough experience, you just know where to start looking".

Right. Cool story.

In my present state of newness, I have two somewhat unreliable, but well-defined techniques.

The first is to ```ag``` my way through the codebase in an effort to information-gather. This doesn't often solve the parse error, but it helps me get the larger context, which is usually important.

The second technique -- because all of our project's JS is compiled to CoffeeScript -- is to write all my code in really vanilla JavaScript, and then manually convert it to CoffeeScript. Sometimes this gives me insight into where my syntax went wrong, or if I'm missing whitespace somewhere, and sometimes....if I'm lucky....all the things start working again.

I wish I knew better options! But I have faith in the gods of Google, that one day a JavaScript wizard will write a blog post, and that blog post will find it's way to me, and then I will know it all.

Amen. 
