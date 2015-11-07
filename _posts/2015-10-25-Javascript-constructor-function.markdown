---
layout: post
title:  "JavaScript Constructor function"
date:   2015-10-25
categories: javascript constructor function
---

#What is a JavaScript constructor function?
Constructor functions are JavaScript objects. It creates a new object and can be created by using "new" like in the example below. The "new" sets the "this" binded to the object.

{% highlight javascript %}
function theObject() {
	this.object = "Object";
}
newObj = new theObject();

{% endhighlight %}

#JavaScript vs Ruby
JavaScript uses literal notation or constructor functions to create a new object. There are a lot more syntax needed in JavaScript than in Ruby as well. JavaScript requires semicolons and parenthesis but Ruby doesn't require as much.

JavaScript
{% highlight javascript %}
function myObject() {
  this.object = "hello";
}
{% endhighlight %}

Ruby
{% highlight ruby %}
Class ObjectOne
  def initialize(name)
    @name = name
  end
end
{% endhighlight %}
