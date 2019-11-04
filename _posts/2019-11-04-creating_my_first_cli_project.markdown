---
layout: post
title:      "Creating my first CLI Project"
date:       2019-11-04 16:53:07 +0000
permalink:  creating_my_first_cli_project
---

Over the past two months, I have learned various new concepts in object oriented ruby. If you had asked me at the beginning of my journey at Flatiron if I could see myself creating a CLI, the best answer I could have given you would have been, "I sure hope so, but I honestly don't know." Becoming a full stack engineer does not go quite the way you expect it to in your own mind. It actually becomes so much more. It has taught me to think abstractly, how to solve a problem and give certain elements functionality. At the beginning of project week, I admittedly felt very intimidated by what was ahead of me. I wasn't sure of myself nor of whether or not I were truly prepared for it. To extent, I was sort of right. I created my project and had it working just fine. However, my cohort lead took a look at it when I was done and found that I wasn't following a rule of single-use programming. 

All of my code was working from within my CLI.rb file. To give a bit of a background about my project, I wrote a CLI that scrapes the Social Security Administration's website for the top 10 most popular baby names of the previous year. I would have done it for this year, but babies are still being born and we still have a couple months to go before we find out the results of 2019. What it comes down to is, my program returned the top 10 baby names for girls and boys.

My cohort lead pointed out that my code could be more organized in terms of applying my methods to their own relative classes. Anything having to do with boys should go in a BoyNames class, anything having to do with girls should go in a GirlNames class, and anything that involves scraping should go in a Scraper class. Everything else, like methods that call a new instance of the CLI to run, should be inside of the main BabyNames::CLI class. Additionally, I failed to apply a new instance for each baby name. My iterations scraped the individual names, but not a single one of them had their own class instance. For the sake of cleaner and professional code, my cohort lead helped to guide my project towards one that was more uniform with great code. 

At this point, it feels as though I have finally accomplished something and went beyond what I ever thought I would be capable of. It's easy to be a dreamer, but it is more rewarding to wake up those dreams and live them. My experience so far has been wildly challenging, but so rewarding at the same time. I never acquired this quality of skill and dedication even having gone through college and acquired an associate's degree. I will be forever thankful for this journey I'm taking, and I absolutely cannot wait to see what just the next 8 months has in store.

On to becoming a greater developer!
