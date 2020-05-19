---
layout: post
title:      "JS w/ Rails as a Backend API"
date:       2020-05-19 17:55:02 +0000
permalink:  js_w_rails_as_a_backend_api
---


Let's get one thing straight -- Ruby on Rails as a Backend API is amazing. My project required using it with JavaScript (JS) as my front end. The hardest part of learning JS was understanding the different syntax. Especially coming from Ruby / Ruby on Rails which many in the IT community say already feels like cheating as a professional dev. JS came with many challenges such as learning how the keyword `this` works in addition to learning the structure and rules for a `fetch()` request. 

I believe what I enjoyed most about the experience, however, was learning important concepts related to JS. To list a few...

## Variable Declarations
Variables are the basic foundation for just about every programming language. In JS, we have three main types: `var`, `let` and `const`. The main one we avoid using altogether because of scope issues is `var`. In place of it, we have `let`, which allows for variables that can be altered, and `const` which allows for variables that cannot be altered. Examples of how they are used are: `const myVar = 'I'm an unchanging string!'` and `let myVar = 'I can be changed!'` These also play a key role in another concept mentioned below: Hoisting!

## Hoisting
Hoisting refers to JavaScript's default nature in declaring variables first before initializing them. Additionally, they are also `hoisted` to the top of their scope. What does this even mean? Think of how it applies to a function. 

`
hoistingFunction = () => {
    a = 10;
		var b = 12;
}`

With the above function, there are two things happening. First, if I try to `console.log(a)`, I will receive `10` as a result. The reason for this is because `a` is an undeclared variable, which automatically makes it a global variable accessible outside of the function. Second, if i try to `console.log(b)`, I will get a `not defined` refference error. This is because `b` is confined to the scope of the function as a declared variable. As previously mentioned, variables are declared before execution and go to the top of their scope. Undeclared variables are executed and belong to the global scope.

## ES6 Syntax
JS hasn't always been as versitile as it is now. It wasn't until 2015 when we received addtions to JS such as `const`, `let`, arrow functions, classes, parameter values and exponentiation (`**`). Arrow functions are not hoisted and therefore have no `this` . That means they are not good for general object structuring. To serve the best purpose, they should also be declared, typically by `const`, before they are executed.

## Conclusion

This was a very challenging project. It also taught me hate Vanilla JS. It takes a lot of code to do the most simple of tasks. I wont go into depth as to why other than the amount of DOM manipulation and AJAX requests needed to make everything run smoothly makes me feel like something can be done to make it quicker and more efficient. With that said, I am looking forward to learning React! I hear very great things about the framework & I'm eager to find out for myself!


