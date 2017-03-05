---
categories: [daily blog]
featuredalt: ""
featured: ""
title: "Day 6"
description: ""
date: "2017-03-04T23:00:48-06:00"
linktitle: ""
featuredpath: ""
---

It was a LONG day of HTML & CSS and I'm still not done with this section. It's okay though. While a lot of it has been review a lot of it has not as well. I've been learning a ton about responsive web design. Especially Mobile Up (Mobile First) design and how to utilize @media queries in CSS to set break points. As well as some best practices doing design of this type. Desktop Down principles were discussed as well but I think at this point in time there is no reason to utilize that methodology. Too many people are utilizing their phones as their primary was to consume content and the trend is moving in that direction anyway.

I think this section feels really long and boring because so much of it is being explained in videos and less with actually coding. Maybe 5-10 lessons to each coding exercise. In addition, most of the coding is codealong so there is much less thinking involved. At least I can set the videos to 1.5x speed. I'm 87% of the way done with this HTML and CSS section so I'll finish it off tomorrow for sure.

I did finally learn why people would use `em` for `font-size` as opposed to pixels `px` or points `pt`.

> It is to our advantage to set all typography within our site to ems and then in media queries adjust the body font-size as a percent to adjust all type in proportion to each other. This greatly simplifies our media queries on typography.

When all the type sizes are relative there is only one thing that needs to change (`body { font-size }`) and all the type on the page will adjust relative to each other. Keeping everything in perfect proportions. Pretty nifty and definitely something that should be done these days as more and more people are utilizing their cell phones for EVERYTHING.

A couple notes I took on Mobile Up:  
To set a wrapper using Mobile Up, first set the wrapper to a % then when the screen gets large enough utilize a fixed width. ie:
```css
.wrapper {
  width: 90%;
}

@media only screen and (min-width: 980px) {
  .wrapper {
    width: 960px;
  }
}
```
Also, to setup multi-column design first utilize a column `width: 100%` and `float: none;` then move to columns being a percentage and floating them. ie:
```css
.column {
  width: 100%;
  float: none;
}

@media only screen and (min-width: 600px) {
  .column {
    width: 33.333%;
    float: left;
  }
}
```
Finally, my last note on design in general is that experts say the optimum readability is 40-80 characters per text line. I guess that's why the break for soft wrapping in [Atom][1] (the editor I've been using as of late) is set to 80 by default.

Time spent today: 7:59  
Time spent total: 27:34  
Lessons completed today: 40

  [1]:https://atom.io/
