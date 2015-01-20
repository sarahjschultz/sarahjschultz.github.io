---
layout: post
title: Run Against Your Bundle
---

Today I could not understand what was going wrong or why. A colleague and I had been working in the same body of code, and his code was merged in and the specs ran and everything was GREEN-GREEN-GREEN.

So I merged his code in and resolved the conflicts from that, which, I shit you not, amounted to a single line of HAML and using an explicit Rails route instead of this decorator method we'd originally used, but that he'd deprecated.

Easy peasy.

So I run my specs. EXPLOSIONS! EVERYTHING FAILED.

WTF?

I spend 30 minutes looking at this. I read StackOverflow about Devise::TestHelpers causing strange ENV failures because they aren't suited to be used outside of your Controllers.  HOW IS THIS RELATED TO ANYTHING ON EARTH?

A colleague pairs with me to troubleshoot -- "Do you always run your tests in RubyMine?", she asks.  "No, I just happened to be trying to troubleshoot here and didn't even consider running from the command line."

We run the specs from the command line. ALL PASS.

Again, wtf.

RubyMine was not running our test suite against our project bundle. For what reason, I cannot tell you because I read all my configurations and RM has all of the correct settings and paths to our gems.

This is witchcraft. And the lesson of the day is to always make sure you are running your tests against your bundle!

