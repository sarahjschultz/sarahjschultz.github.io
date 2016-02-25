---
layout: post
title: Read All of Rubocop
---

Today I decided to start small, you know, because that is what smart people do. 
So Day 1/30 is: read through all of the issue queue for the [Rubocop](https://github.com/bbatsov/rubocop) gem.

Do you use that gem? I fucking love it. You know why?  
Is there anything ON EARTH that is more soul-sucking than arguing with your colleagues, 
during Code Review about something that THE ENTIRE COMMUNITY HAS AGREED is a style standard?
I cannot think of a single fucking thing that is worse than that. 

Oh, you LIKE IT BETTER when you have a 40 line comment describing the User story for this particular 3 line method?  
Tell me more about your feelings.

No.

Anyway, with Rubocop, I never even have to use a single breath on this issue. 
Not a SINGLE keystroke gets dedicated to that ass-hattery.  
Why? Because the build just FAILS.  

You don't want to format your code?   
You refuse to adhere to styleguides?    

That's cool, you do you. Your code just...you know, isn't going out.    

So it saves me a lot of really silly talking about things that I would  
rather not talk about.

Anyway, I read through their entire repository and issue queue.   
It was cool! I learned a thing, here I'll show you: 

```  
a = if false  
       'def'
    else 
      nil
    end

a.nil? # = true  

a = 'abc'
a = if false
      'def'
    end

a.nil? # = true
```  
In Ruby, an if-clause necessarily assigns nil if it evaluates to false.  
What's interesting about that, are those gnarly conditionals that you sometimes see in some projects that are like:  
  
```  
a = if thing_that_could_be_true_or_false
      pass_this_thing
    else
      nil
    end
```

So that else can just GO AWAY. 

Pretty cool, right?  
Rubocop has this Style/EmptyElse cop that enforces that little magic.  

Who knew? Well, besides the people who wrote it and obviously use it and knew it already.
