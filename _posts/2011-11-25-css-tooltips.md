---
layout: post

title: CSS tooltips
summary: How to use the `:before` and `:after` pseudo-elements to create CSS tooltips.

category: post
---
Tooltips are fairly common these days because they are a great way of providing a little extra context or information to a user before they perform an action&sup1;.

One of the more common solutions has been [tipsy](http://onehackoranother.com/projects/jquery/tipsy/); a jQuery plugin for creating tooltips based on an anchor tag's `title` attribute. While this plugin works a treat, there are leaner options available.

I've written up a CSS-only alternative to displaying tooltips which uses a data attribute and the `:before` and `:after` pseudo elements. The `:before` pseudo element handles the arrow and the `:after` takes care of the body of the tooltip.

View the [demo page](http://adamwhitcroft.com/lab/css-tooltips/) or head straight to the [GitHub repository](https://github.com/AdamWhitcroft/CSS.Tooltips).

&sup1;<small>In most cases, tooltips are used in conjunction with an anchor.</small>