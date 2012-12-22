---
layout: post

title: Gravatar as favicon function
summary: A small PHP snippet that sets your Gravatar image as your site's favicon.

category: post
---
I like how Tumblr uses the blog author's Gravatar as the site favicon. I thought it would be fun to replicate that with a Wordpress site so I came up with a simple function to do so.

    function GravatarAsFavicon() {
    $GetTheHash = md5(strtolower(trim('YOU@YOURDOMAIN.COM')));
    echo 'http://www.gravatar.com/avatar/' . $GetTheHash . '?s=16';
    }

And then, in your document `<head>` add the following:

    <link rel="shortcut icon" href="<?php GravatarAsFavicon(); ?>" />