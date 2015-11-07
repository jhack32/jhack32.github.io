---
layout: post
title:  "Enumerable Methods"
date:   2015-10-10
categories: enumerable methods ruby
---

#What is the group_by method? 
It is a Enumerable method. Enumerable is a module that contains multiple methods we can use. The group_by method is similar to a loop. The group_by method takes in a collection of objects and outputs a hash. The keys are the evaluated result and the values are the arrays of the elements (values from the input). It can take a set of numbers (1..6) and go through the loop performing the block of code for each number.

{% highlight ruby %}
(1..6).group_by {|x| x % 3} #=> {0=>[3, 6], 1=>[1, 4], 2=>[2, 5]}
{% endhighlight %}

This is the same example shown in Ruby Docs. It will go through numbers 1-6 and run the block, which is the number modulus 3. The numbers that are divisible by 3 without any remainder, will be in the 0 key (3,6). The group_by method does literally what it's called. It groups the object's it's given into a hash and follows the block of code it's given.

#What is the map method?
The map method is an Enumerable method as well. Map has a destructive (map!) and non-destructive form (map). The destructive form will change the values permanently and a non-destructive form doesn't. It's the same exact method as collect. The difference between the two is the name. People can look at it in two ways. The first would be doing something then collecting the result and the second way would be re-mapping the original object.

{% highlight ruby %}
a = [1,2,3,4]
a.map {|x| x + "..."} #=> ["1...", "2...", "3...", "4..."]
a #=> [1,2,3,4]
a.map! {|x| x + "q"} #=> ["1q", "2q", "3q", "4q"]
a #=> ["1q", "2q", "3q", "4q"]
{% endhighlight %}