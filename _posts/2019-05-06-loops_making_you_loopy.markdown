---
layout: post
title:      "Loops Making You Loopy?"
date:       2019-05-06 13:27:29 +0000
permalink:  loops_making_you_loopy
---


Loops were one of the first things I learned when I started coding. It was hard to wrap my head around at first but after I understood a few key take aways it became a lot more simpler. Loops are a way to control the flow of your statements in your programs. 


## for loop 
```
for i in 1..3; 
puts "The value of the variable is #{i}.";
end
``` 

The output would be cycled through 1 2 and 3 respectively for that many times. Although the same thing can be accomplished with iteration, it's kind of a neat way to solve a problem. 


## while loop
```
counter = 0;
while counter < 3; 
puts "This will repeat 3 times"; 
counter+= 1;
end
``` 

## until loop 
```
var = 3 
until var == 5 do 
puts "var isn't equal to 5"
var += 1 
end
```

The until loop has always been my favorite for some reason. It just seems more straightforward and easier to implement. 


The most interesting thing about loops to me though is how easy it is to forget to put the right condition in your loop to make it stop. 

## infinite loop 
```
loop do 
puts "Infinity and beyond!" 
end
```

Alternatively to have a little more control with some of your loops you can use the break keyword to stop a loop when you want to.



