---
layout: post
title: "CSS Concepts"
date: 2015-09-26
categories: css concepts
---

# What are the differences between relative, absolute, fixed, and static positioning?

The position values could get a little confusing. I was confused my first time using the values. I'm going to try my best and explain what each one does. The relative position places the element in relation to its normal position. So if we were to apply top, bottom, right, left to the element along with position: relative, it will be adjusted away from the normal position.So it'll move from `A --> B`. Once you have adjusted the element with relative positioning, other elements won't be able to fit into any whitespace (empty space) the element takes up.

{% highlight css %}

.randomclass { position: relative; top: 0; bottom: 0; right: 10px; left: 0;}

{% endhighlight %}
The above code will place the elements with the class (randomclass) in a position relative to the original and move it away 10px to the right.

`Absolute position` is placed at a specific position in relation to the closest element. The position also has the ability to move along with the page if there are no positioned elements (position elements includes everything except static) before it.

{% highlight css %}

.randomclass { position:absolute; left: 5px; top: 50px; }

{% endhighlight %}

The above code will move the element with the class (randomclass) to the LEFT 5px and TOP 50px. It can move the element anywhere you want to.

`Fixed position` stays in the same place throughout the entire website. If you created a navigation bar and set it to fixed, it will follow you as you scroll down the page.

{% highlight css %}

.randomclass {position: fixed; bottom:0; border: 1px solid black; }

{% endhighlight %}
This sets the element in a fixed position on the bottom with a 1px solid lined black border.

The `default position` is `static`. This position isn't affected by the top, bottom, right, left properties. Static is positioned to the flow of the page. Top to bottom from the left.