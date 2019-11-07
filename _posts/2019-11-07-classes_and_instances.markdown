---
layout: post
title:      "Classes and Instances"
date:       2019-11-07 22:45:38 +0000
permalink:  classes_and_instances
---


While learning the basics of Ruby, we come across the wondeful uses of classes and instances of those classes. Of course, this was among some of the more intense concepts of programming. However, understanding the logic behind it comes easier when you give yourself the time and patience to understand them. So, just what are classes and instances?

Classes are inherently objects. In Object Oriented Programming (OOP), none of the objects we create are real objects. They are, however, molded by the idea of what an object is. Take yourself as an example. You could be considered an object that is part of the Human class. If we are comparing the coding concepts to real life, you are what is known as an instance of the Human class. Alas, you are not the Human class itself since you are not every human that ever was nor are you the container that holds them. Therefore, you must be an instance.

Let's take a look:

```
class Human
    attr_accessor :name, :age, :gender
		
		@@all = []
		
		def initialize(name, age, gender)
		    @name = name
				@age = age 
				@gender = gender 
		end 
		
		def self.all 
		    @@all
		end 
end 
```

This is what a Human class would look like. We could also include `weight` , `height`, `personality`, etc. But for now, let's keep things simple with `name`, `age`, and `gender`. If we wanted to create an instance of the Human class, this is how we would do it below. In this case, let's create an instance for the Hulk!

```
hulk = Human.new("Hulk", 30, "Male")
```

Now, the Hulk is a new instance of the Human class. He may be able to turn into a big green monster, but he is still a human after all... right?

An instance can have multiple values, but the Hulk here has just three: his name, his age, and his gender. We wouldn't be able to pull those values from the class itself since those values are undefined and too generalized outside of an instance. These concepts reflect on the difference between a class and an instance of a class. In conclusion, a class is like a blueprint for a large building while the instances of those classes are the building blocks that we are trying to put together.
		



