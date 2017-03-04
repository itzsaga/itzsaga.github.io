---
author: ""
categories: [daily blog]
date: 2017-03-03T04:27:10Z
description: ""
featured: ""
featuredalt: ""
featuredpath: ""
linktitle: ""
title: Day 4
---


Today was no longer than the first few but definitely felt like it was. I learned the hard lesson that with this schedule I actually have to go to sleep when I schedule it. I stayed up late last night but still stuck to my 6 am wake-up call. Needless to say my last 30 minutes of coding tonight was not good and I couldn’t make progress like I know I can. I’m just foggy in the head and tired. My prime nap time in the middle of the day was taken away by my grumpy 2.5-month-old who 3 minutes after I set a 30-minute alarm for my nap decided she would cry for 90 minutes. I finally got her calm and **boom** my 2-year-old is awake from her nap. I love them both, I just really would have enjoyed that nap today.

Nothing big happened today in my schooling. The people that wrote the curriculum like to include quotes here and there and I saw one name pop up a few times so I looked him up. Turns out [Edsger W. Dijkstra][1] was a pretty big deal in the world of CS and programming. I didn’t read his entire Wikipedia page but I intend to.

One other thing stuck out today. The fact that `#detect` and `#find` do the same exact thing. This is actually one reason that I was so stuck tonight. With the way that Flatiron is setup, every successful lab is public on GitHub. If I’m really stuck I’ll look at how others solved the problems for inspiration. There is rarely one answer so I’ll take the code I have and look at say 5 other people’s solutions and get my brain moving again. I kept seeing `WIN_COMBINATIONS.find` and I was thinking, “Where did these people learn this `#find` method? So I went to the ruby docs and realized that it was the same exact thing as `#detect` when I saw this:
```ruby
(1..10).detect   { |i| i % 5 == 0 and i % 7 == 0 }   #=> nil
(1..100).find    { |i| i % 5 == 0 and i % 7 == 0 }   #=> 35
```
To make it even worse, I had earlier written down on my pad that these were the same thing so I wouldn’t forget to blog about it tonight.

> NOTE: detect and find are two names for the same method. For every example below we’ll use detect, but you can use them interchangeably.

How does this even happen though? Why would the person or people who wrote a coding language choose to make two words do the exact same thing?

That’s all for now. Still need to walk the dog, setup my coffee for the morning, and throw some stuff in the dryer.

Time spent today: 2:32  
Time spent total: 12:13  
Lessons completed today: 12


  [1]: https://en.wikipedia.org/wiki/Edsger_W._Dijkstra
