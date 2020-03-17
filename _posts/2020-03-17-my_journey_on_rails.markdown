---
layout: post
title:      "My Journey on Rails"
date:       2020-03-17 11:07:39 -0400
permalink:  my_journey_on_rails
---


## The Start

When it came to Ruby on Rails (RoR), my classmates and I went in with a lot of confidence. Since completing our Sinatra projects, we naturally began feeling like this journey was really starting to pay off. After all, that was the point in which we started working with web pages rather than just building CLIs and logging results in our consoles. In my case, I was especially challenged when my daughter was born right before starting to learn Ruby on Rails. Along the way, though... I started to become discouraged. There was a lot of information to take in, and retaining it was nearly impossible. I was beating my head against the wall most days, but I eventually realized that I had it ***all wrong.* **

I would go out of my way to make desperate Google searches such as, "How do programmers retain everything they learn?" Come to find that we ***don't***. Understanding that was difficult to accept. I could only wonder, "How are we supposed to truly be efficient without retaining 100% of the things we learn?" It was never outside the realm of possibility with repetition, but I eventually learned from industry professionals 20 years in the field that they continuously reference even the simplest of code. That's when it finally clicked... *learning to be a programmer is about learning how to code, not memorizing it*. Memorization, again, comes with repetition. However, the point is to understand the logic and laws within the syntax of whatever language you're working with.

## Forms

With that said, the hardest part for me was learning how to use forms for database relationships. In addition to that, fully understanding how the `has_many, through:` relationships worked inside of RoR also came as a challenge. Naturally, it was because of how the forms were set up. Here is an example:

```
    <div>
        <%= f.label :project_id, "Please choose the project for this task:" %><br>
        <%= f.collection_select :project_id, Project.all, :id, :name %>
    </div>
```

If you look at `f.collect_select :project_id, Project.all, :d, :name` , the `f` represents the parent object for the query. In this case, it is `tasks`. We are selecting the `:task` as the field namespace, getting the field name `:project_id` id from the array or collection `Project.all`, and making our associations using the `:id` method call for every row, and specifying our `params` with `:name`. This is how we manage to link our relationships in forms.

## OmniAuth

I also want to cover this beast of a problem. OmniAuth was really hard to get working since I had to find out the hard way that user model validations can stop OmniAuth from working if certain parameters aren't needed to pass such as user account first and last names. They are provided by the auth providers as `:name`. This forced me to discover the use of `@user.errors` within a `binding.pry` to figure out how to solve my problem. The solution I came up with involved setting conditional statements inside of my controller for when certain validations need to be active. In my case, I set my validations for `:first_name` and `:last_name` as inactive if `@user.provider = "facebook".`  Which is hard-coded/declared ONLY during the third party authorization process.

## Conclusion
I definitely feel like I've grown as a web applications developer. I have spent many hours coming to understand this wonderful framework. I still have much to learn, but I am humbled by every step of the way. Here is to continuing my growth and becoming the best software engineer I can be!
