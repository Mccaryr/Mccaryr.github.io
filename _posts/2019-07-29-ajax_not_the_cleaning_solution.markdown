---
layout: post
title:      "Ajax, Not The Cleaning Solution"
date:       2019-07-29 15:44:39 +0000
permalink:  ajax_not_the_cleaning_solution
---


My latest project I worked on making apps more responsive. I was really excited about learning this, because it fundamentally changes how our apps work. By frontloading our logic we can get extremely fast responses back without the site redirecting. What I didn't realize was, how complicated this was without  remote: true. There are so many things going on in the background of making an Ajax request that it will give you a deep appreciation of how technology works. First, you have to hijack a link by copying the id or class and prevent the default of redirecting. Then you have to make the request as well as making sure it's in the correct format AND then append it to the DOM. There's also a million and one things going on, but that's the cliff notes. The hardest part I had with this project was  dealing with multiple associations and getting the ID's of a belongs_to form submission. One of my proudest and most hacky way of dealing with a form submission.

```
let id = $(this).attr('action')[7];
$.post('/posts/'+id+'/comments', values) 
``` 


When I was submitting my comment form I didn't have access to my Post construct and I couldn't find out anyway to use a belongs_to association to access my Post's info. The this keyword only gave me access to the actual form submission information. The only useful thing with an ID was the action. So I was able to use that to emulate the ID. Looking back though Regex would be a much cleaner solution. Overall this project was frustrating, but I learned a TON about Ajax and how to troubleshoot in general with JS. 



