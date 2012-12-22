---
layout: post

title: A simple Wordpress calendar
summary: No plugins or no custom post types required, just a `query_posts` function and a custom field within a post.

category: post
---
Here's a quick way to turn a category of posts into a simple calendar using nothing more than a custom field and WordPress' `query_posts` function; no plugins or custom post types required.

##Setup

Create a new Posts category called 'Events'. We'll use this category name in the `query_posts` example, but you can name it anything you like. Apart from keeping the backend organised, having a separate category for these posts makes them dead easy to use in custom queries.

Create a new post, add a custom field called 'date' and assign the date of the event as the value. You'll need to format the date in a specific way for this to work.



##Date format

It's best to format your event date like so: `YYYY-MM-DD`. This ensures the sort parameter within the `query_posts` function works as it should.

##The code

Add the following snippet just before the loop on the page you'd like to display the list of events, in this case I created a new page called page-events.php

    <?php query_posts(array( 'category_name' => 'Events', 'meta_key' => 'date', 'orderby' => 'meta_value', 'order' => 'ASC' )); ?>

That's all there is to it really.

Here's a more detailed example which includes our custom query, the loop and some basic markup.

    <?php query_posts(array( 'category_name' => 'Events', 'meta_key' => 'date', 'orderby' => 'meta_value', 'order' => 'ASC' )); ?> <?php if(have_posts()) : while(have_posts()) : the_post(); ?> <div class="post event"> <h3><a href="<?php the_permalink(); ?>"><?php the_title();?></a></h3> <p class="date"><?php echo get_post_meta($post->ID, 'date', true); ?></p> <p><?php the_excerpt(); ?></p> </div> <?php endwhile; ?> <?php else : ?> <p>Sorry! No events could be found</p> <?php endif; ?> 