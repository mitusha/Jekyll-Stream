---
layout: post

title: Random message generator
summary: Because every website needs a random message generator. 

category: post
---
If you're looking for a quick and easy method of generating a random message&mdash;perfect for a greeting on your website&mdash;give this a go.

    function randomMessage(){ 
    	$messages = array( 
    		"A message", 
    		"Another message", 
    		"Another another message" 
    		); 
    	$generateMessage = $messages[array_rand($messages,1)]; return $generateMessage;
    }

Simply call the function where you'd like to use it with `<?php echo randomMessage(); ?>`