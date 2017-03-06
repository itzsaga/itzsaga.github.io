---
categories: [daily blog]
featuredalt: ""
featured: ""
title: "Day 7"
description: ""
date: "2017-03-05T22:05:48-06:00"
linktitle: ""
featuredpath: ""
---

After 3 hours today I finished up the HTML and CSS section. I took one real note today in that 3 hours:  
When it comes to [Bootstrap][1] as a framework the `.col-xs` class never stacks vertically no matter how small the width of the screen gets. Figured that was something I might need to know later. I also learned a lot about how powerful and easy it is to make a site responsive using Bootstrap. I had used Bootstrap in the past but never really understood how to use it more fully.

I also spend a chunk of time troubleshooting the custom Learn IDE (built on top of Atom) that Flatiron provides. It has some quirks. Very simple the workflow is this, click a button on the site, the IDE opens, runs a command to fork then clone down a GitHub repo with all the files you need. There were a couple labs that had zero files in them. However, I was building on a previous lab so I had the files I needed. I copied and pasted them into the appropriate place in File Explorer but the IDE wouldn't show them. I had to "Import" them from within the IDE for it to acknowledge their existence. This was a pain in the ass to say the least.

I'm finally back into Procedural Ruby. Funny thing is I'm coming across labs that directly relate to the ones that I did in the Bootcamp Prep course. They're carbon copies in fact. The only difference is that I chose to do the JavaScript Bootcamp Prep and now I'm solving problems in Ruby. It's interesting though to see how different languages solve the same problems.

Of course I have to give an example. Here's the modified (to make it make more sense for both languages) Deli Counter lab requirements:

1.  Build the method/function that shows everyone their current place in the line. If there is nobody in line, it should say `"The line is currently empty."`.
2.  Build a method/function that a new customer will use when entering the deli. The method/function should accept two arguments, the array for the current line of people, and a string containing the name of the person wishing to join the line. The method/function should return the person's  name along with their position in line.
3.  Build a method/function which should call out the next person in line and then remove them from the front. If there is nobody in line, it should call out that `"There is nobody waiting to be served!"`.

First is JavaScript:
```javascript
var katzDeliLine = [];

function currentLine(x) {
    var line = []
    if (x.length === 0) {
      return "The line is currently empty."
    } else {
      for(var i = 0; i < x.length; i++) {
        line += (i + 1) + ". " + x[i] + ", "
      }
      line = line.slice(0, line.length-2)
      return "The line is currently: " + line
    }
}
function takeANumber(katzDeliLine, name) {
  katzDeliLine.push(name)
  return "Welcome, " + name + ". You are number " + katzDeliLine.length + " in line."
}
function nowServing(x) {
  if (x.length === 0) {
    return "There is nobody waiting to be served!"
  } else {
    var name = x[0];
    x.splice(0, 1);
    return "Currently serving " + name + ".";
  }
}
```
And then in Ruby:
```ruby
katz_deli = []

def line(x)
  line_array = []
  if x.length == 0
    puts "The line is currently empty."
  else
    x.each.with_index(1) do |name, index|
      line_array.push("#{index}. #{name}")
    end
    puts "The line is currently: #{line_array.join(" ")}"
  end
end
def take_a_number(katz_deli, name)
  katz_deli.push(name)
  puts "Welcome, #{name}. You are number #{katz_deli.length} in line."
end
def now_serving(array)
  if array.empty?
    puts "There is nobody waiting to be served!"
  else
    puts "Currently serving #{array[0]}."
    array.shift
  end
end
```
A small thing I noticed is that it took me 3 less lines of code to do it in Ruby. I'm sure I'm not as eloquent in JS as I could be though so I'm sure that could be condensed down as well.

Finally, I laughed when I read about the "spaceship" operator `<=>` only because it's nicknamed that because it looks like a flying saucer.

On a personal note. This schedule I set is rough. Not really on me as much as on the family. It's hard to lock yourself in an at home office for 12+ hours a day 3 days a week with a 2 year old and a 2 month old at home. It takes a lot of work watching over them and when both of us are home it's definitely easier for both of us to contribute. I still think next week I can break the 45 hour mark for the amount of time I get to work on coding. I had planned on 52 hours a week which would have me done with the ~800 hours of curriculum in 13 weeks. Since I pay by the month if that gets pushed a couple weeks I'll still be done <16 weeks and not pay for that 5th month.

Time spent today: 5:52  
Time spent total: 33:26  
Lessons completed today: 32

  [1]:https://getbootstrap.com/
