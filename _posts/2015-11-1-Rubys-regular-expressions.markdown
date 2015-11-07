---
layout: post
title:  "Ruby's Regular Expressions (regex)"
date:   2015-11-01
categories: ruby regex regular expression
---

#What are regular expressions?
`Regular Expressions` are "patterns which describe the contents of a string." It helps us find a set of characters.

#What's the usage?
Regular expression helps us find/match characters a lot easier. We use symbols in regex that start off with a / and end with /. The symbols are all different and have their own uses. For example, the | symbol would represent OR (similar to ||). \s is for whitespace. 

{% highlight ruby %}
\D #=> Matches anything but a digit
numbers_only = 1234-1232.123213/512321
numbers_only = numbers_only.to_s.gsub!(/\D/, "")
puts "Output: #{numbers_only}"
#=> Output: 1233997595017161

{% endhighlight %}

Regular expressions help us find characters we want a lot quicker and easier. It's DRYer as well. We can also edit what we find by replacing/subbing it. Regular expression may be hard to understand at first but will become easier as you start to use it.

