---
layout: post

title: CSS3 Gmail Buttons
summary: 42 buttons with 3 colours in the style of the sleek new Gmail GUI.

category: post
---
I've wanted to create a button pack for a while but I've never really had any inspiration to do so. Social Media buttons have been done just about to death so I didn't want to spend time contributing to an already saturated pool. I logged into Gmail shortly after their redesign and I like what I saw. A lot.

View the [demo page](http://adamwhitcroft.com/lab/css3-gmail-buttons/) or head straight to the [GitHub repository](https://github.com/AdamWhitcroft/CSS3.Gmail.Buttons).

I had planned on using the [Iconic Icon Set](http://somerandomdude.com/work/iconic/) as the base for the icons, but the style didn't quite sit right so I threw caution (and a few evenings) to the wind and created the icons myself. I didn't want to use any dithering or anti-aliasing techniques for the icons, opting instead to keep them perfectly crisp. 

The buttons themselves were made to be as simple to implement as possible so they use multiple classes which build upon each other, allowing a great deal of flexibility. It all starts with the base class `class="bttn`. This will result in the most basic of the button styles. From there, you have the option of adding a number of additional classes depending on the button you would like.

There are 3 colour styles and a total of 42 icons that you can use, as well as an emphasis class which sets the button text to all caps; a great way to make a specific button really stand out. There are also 2 options for grouped buttons and a preset perfect for pagination.