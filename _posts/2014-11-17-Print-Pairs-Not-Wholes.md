---
layout: post
title: Print Pairs Not Wholes
---

The other day I had to write a gnarly rake task to iterate through 30,000 records, ask some things about those records, and then organize them into bins based on what the answers to those questions were.

I had determined that the best structure for this would be to use a Hash, because one record could have multiple answers to a given question, and key-value pairs are money, when the value is an array of answers to my questions.

But this is also a somewhat gross structure to try and bounce around in, because things can get squirly when you get deep inside of blocks of blocks of blocks.  Especially for me(!), as I am still learning all the things.

A practice that I’ve been using, is to make sure that I test each layer of the task, by printing to the console, whatever it is that I have, and then making sure that it IS what I think it is.

But when you are new, you do a lot of things wrong, and so today’s record of Things I Did Wrong goes like this:

When you ```puts``` the _entire_ hash, this is really different than when you ```puts``` the specific key:value pair that you’re working with.

And you might not notice this when you initially run the task, because maybe you’ve only been through 10-15 records, and only made 2-3 matches.

But when you are in the other room, and you hear the fan on your MBA start sounding like a Cape Canaveral liftoff moment, you realize that going through 30,000 records and then printing the _entire_ hash at every pass through the loop, gets to be really intense and is a really bad idea.

If you don’t know, now you know.