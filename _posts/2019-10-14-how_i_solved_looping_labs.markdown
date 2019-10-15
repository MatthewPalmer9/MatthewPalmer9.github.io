---
layout: post
title:      "How I Solved Looping Labs"
date:       2019-10-15 02:27:02 +0000
permalink:  how_i_solved_looping_labs
---


Loops are one of the harder concepts to grasp as a new programmer since the logic behind them can be a bit offputting. One of the struggles behind understanding how they work comes down to making sense of it in English in concern to what exactly is happening. Below is a simple example of a loop:

```
count = 1

while count < 10
   puts "Hello, I am count number #{count}!"
	 count += 1
end 
```

To tell you the truth, all code makes better sense if you can break down the logic and teach it back to yourself in English. Let's start from the top down (Doesn't that sound familiar to the way code blocks work?).
Our 'count' variable is keeping track of itself -- the count! We set it at 1 in this case since we will begin our counting from 1. What the code block below it is doing in English is just that: "Hey, while the value of count is LESS THAN ( < ) the integer 10, I want to puts this string to my ruby terminal and then add the value of 1 to the current value of count. I want this same process to happen over and over until count is no longer LESS THAN 10."

If "count += 1" was not a factor in our while loop, this would be an infinite loop (read: never-ending). The reason for this is because "count" would ALWAYS be equal to 1 and would never change. However, thanks to our incrementer (count += 1), count adds 1 to its current value every single time the loop happens. Eventually (and very quickly), count will be set to 10 and this will ultimately end the while loop. 

**Conclusion**

The concept of loops are best understood in English. Since the process of code executes in patterns around blocks, it can be difficult to follow on a computational level. My looping labs were solved using what I would like to refer to as the "conversational method", which simply implies that we learn to understand how loops, and any code for the matter, work by first translating the process happening into a simple, English sentence that could be used in everyday conversation. Although programming is logically driven, it's okay to take an abstract approach towards better understanding. After all, we are lazy programmers who seek the easiest and most efficient way of doing things. ;)

