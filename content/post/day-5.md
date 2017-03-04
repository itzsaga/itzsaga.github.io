---
author: ""
categories: [daily blog]
date: 2017-03-04T04:57:01Z
description: ""
featured: ""
featuredalt: ""
featuredpath: ""
linktitle: ""
title: Day 5
---


Today had a rough start. We decided to start potty training today and my wife and I were not on the same page about what that would look like in terms of the amount of coding I would get done today. Thankfully we got things moving pretty smoothly about noon. I then proceeded to complete my first part of the Intro to Ruby curriculum! I now have a functioning CLI Tic Tac Toe game built in Ruby. It can be found [here][1]. Pretty proud of myself for this one. I got stuck on one part and had to do a screen share with what is called a "Learn Expert" but it was actually a quick fix. I was stuck on utilizing a ternary. I had the following problem:
```ruby
# This is passing tests
if draw?(board)
  puts "Cats Game!"
else
  puts "Congratulations #{winner(board)}!"
end
# This is not passing tests
draw?(board) ? puts "Cats Game!" : puts "Congratulations #{winner(board)}!"
```
I couldn't figure out why. Turns out I needed to just put `puts` in front of the ternary because it was going to do that action to either result of the code. This quick fix had my one line solution passing the rspec tests.
```ruby
puts draw?(board) ? "Cats Game!" : "Congratulations #{winner(board)}!"
```
This puts me at 78% of the way through the Intro to Ruby curriculum so I hope to finish that, or be very close to finishing that, today!

Just like that, before 5 pm I just finished the Into to Ruby track by refactoring my Tic Tac Toe code from before. I now have a CLI Tic Tac Toe game that utilizes Object Oriented programming which can be found [here][2]. I've gotten into a good groove and think utilizing the Pomodoro technique is key on these long days. It allows me time to break away for a bit. I'm 42 minutes on and 18 minutes off right now. A key takeaway from this short intro to OO programming is that "an object in code is a thing with all the data and all the logic required to complete a task." I think this sums up an object well and I've always struggled with figuring this out.

> I thought of objects being like biological cells and/or individual computers on a network, only able to communicate with messages. - Alan Kay

Next up are some sections that I think will go quickly:

 1. Git and GitHub
 2. HTML and CSS
 3. Procedural Ruby (only because a bunch of this is done already from this Intro course)
After that is a large chunk, for good reason, on Object Oriented Ruby. I hope to get through all the lessons and labs for this by the end of the weekend and be working on the "Final Projects" for Ruby starting Monday. I think I can do it! We'll see what reality dictates, though.

I was right about the Git & GitHub section. Finished that in ~45 mins. Helps that I've been using GitHub for a while. At the end of the section was this:
![git_comic][3]

HTML and CSS are taking longer than I expected because there are code along videos and there isn't really a way to run through those too quickly.

It was a productive day.

Time spent today: 7:22  
Time spent total:  19:35  
Lessons completed today: 53


  [1]: https://github.com/itzsaga/tic-tac-toe-rb-v-000
  [2]: https://github.com/itzsaga/oo-tic-tac-toe-v-000
  [3]: https://res.cloudinary.com/sethalexander/v1488603381/ieji7xddaoyf6c87zmyg
