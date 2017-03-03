---
author: ""
categories: [daily blog]
date: 2017-03-03T18:59:01Z
description: ""
featured: ""
featuredalt: ""
featuredpath: ""
linktitle: ""
title: day 5
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


  [1]: https://github.com/itzsaga/tic-tac-toe-rb-v-000
