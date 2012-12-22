---
layout: post

title: Per post custom CSS for Wordpress
summary: An easy, plugin-free way to give your Wordpress blog art-directed posts. 

category: post
---
*This post assumes you have basic working knowledge of Wordpress and the ability to edit theme files without ballsing up your site.*

In your header.php file, add the following inside the `<head>` just before the closing tag.

    <?php if (is_single()) { $themeRoot = get_bloginfo('stylesheet_directory'); $customFolder = "customCSS"; $stylesheetName = get_post_meta($post->ID, 'custom_css', true); if ($stylesheetName) { ?> <link rel="stylesheet" href="<?php echo $themeRoot . '/' . $customFolder . '/' . $stylesheetName ?>"/> <?php } }?>

There are 2 things to pay attention to in that snippet.

* The name of the folder storing our custom stylesheets: `customCSS`.
* The name of the custom field we'll using to point to our stylesheet: `custom_css`.

These are names I've chosen for my own website, if you decide to use a different folder or custom field name just amend the snippet accordingly.

Once you've got that, all you need to do is create a new custom field called custom_css in the post you'd like to add your custom styles to. The name of the stylesheet (including the .css extension) goes in the 'value' field.

##The upshot

Using this method, as opposed to relying on `<body <?php body_class();?>>` to generate a post-specific body class which you use in turn to style child elements, ensures you aren't loading up a bunch of code written to style other posts; you are only loading styles that are relevant to the content on screen.

While this method is arguably best suited to adding a little extra polish to a post, this could be extended to create an entirely art-directed blog. You'd need to cover the design of your home page with the global style.css as well as rudimentary layout, but the rest could be done on a per post basis.

##Are there other options?

Yup, you should check out [Anchor](http://anchorcms.com/) or the [Art Direction Wordpress plugin](http://wordpress.org/extend/plugins/art-direction/) which can be seen in action on [Trent Walton](http://trentwalton.com/)'s website.

[Daryl Ginn](https://twitter.com/daryl) has put forward [another method](http://cl.ly/2F2m080x050I0j021d0e) that's worth checking out.