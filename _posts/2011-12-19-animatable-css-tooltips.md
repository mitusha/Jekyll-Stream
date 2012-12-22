---
layout: post

title: Animatable CSS tooltips
summary: Animatable CSS tooltips

category: post
---
Following on from the CSS Tooltips I posted a little while ago, I offer up another solution.

These differ from my original post both in markup and function. The original tooltips made use of the `:before` and `:after` pseudo-elements and while this is probably the most succinct method the major downfall is that CSS animations and transitions can not, at this time, be applied to pseudo-elements.

With only a minor change in the markup, these tooltips are completely animatable.

View the [demo page](http://adamwhitcroft.com/lab/animatable-css-tooltips/) or head straight to the [GitHub repository](https://github.com/AdamWhitcroft/Animatable.CSS.Tooltips).