---
layout: post
title: Read All of Rubocop
---

Today I decided to start small, you know, because that is what smart people do, and to read through all of the issue queue for the Rubocop gem.

Do you use that gem? I fucking love it. You know why?  
Is there anything ON EARTH that is more soul-sucking than arguing with your colleagues during Code Review about something that THE ENTIRE COMMUNITY HAS AGREED is a style standard?
I cannot think of a single fucking thing that is worse than that. 

Oh, you LIKE IT BETTER when you have a 40 line comment describe the User story for this particular 3 line method?  
Tell me more about your feelings.

No.

Anyway, with Rubocop, I never even have to use a single breath on this issue. Not a SINGLE keystroke gets dedicated to that ass-hattery.  
Why? Because the build just FAILS.  You don't know how to format your code? You refuse to adhere to styleguides?  

That's cool, you do you. Your code just...you know, isn't going out.  

Anyway, today I read through the entire repository and issue queue.  It was cool! I learned a thing, here I'll show you: 

```ruby
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
In Ruby, an if-clause necessarily assigns nil if it evaluates to false. What's interesting about that, are those gnarly conditionals that you sometimes see in some projects that are like:  
```ruby
a = if thing_that_could_be_true_or_false
      pass_this_thing
    else
      nil
    end
```

So that else can just GO AWAY. 

Pretty cool, right?  Rubocop has this Style/EmptyElse cop that enforces that little magic.  Who knew? 
