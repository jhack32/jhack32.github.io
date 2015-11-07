---
layout: post
title:  "Ruby Classes"
date:   2015-10-18
categories: ruby class oop
---

#What is a ruby class?
`Classes` are like a class in high school or college. It's specific and does something within the subject. An example would be an American history class would teach everything about American History. In a class called Board, it may contain methods that creates a board or anything that involves a board.

{% highlight ruby %}
class Board
  attr_reader :size
  def initialize(size)
    @size = size
  end
end
new = Board.new(16)
new.size #=> 16
{% endhighlight %}

#What's the point?
There are a lot of benefits to using Classes. One benefit is it helps with organization. It's like a blueprint for the code. It also helps with preventing from variables/methods from overlapping from each other. Without using classes and just having multiple methods is like having a messy room. There's things everywhere but not organized.

#Classes compared to real-life objects
We can think of classes like a room. So let's say that every bedroom consist of 1 bed, desk, chair, computer, and a tv. This will be in your initialize method (in the class). This means that everytime you create an instance of the class (create a new bedroom), it will have a bed, desk, chair, computer and a tv. The attr_accessor will allow us to change the values of our bed, desk, chair, computer, or tv. We can add more than one chair to our room (change value of our chair). The things (watch tv, sleep, etc) you can do in your bedroom would be the methods in a class. It's the function of the bedroom. We could watch tv, sleep or go on the computer. It's things we can do inside the bedroom (class). Instance variables would be similar to the color of the walls or design of the room. It exists only within that room (instance of the class).

{% highlight ruby %}
class Bedroom
  attr_accessor :bed, :desk, :chair, :computer, :computer, :tv, :wallcolor
  def initialize(name, wallcolor)
    @name = name
    @wallcolor = wallcolor
    @bed = 1
    @desk = 1
    @chair = 1
    @computer = 1
    @tv = 1
  end
  def sleep
    puts "zzzZzzzZzz"
  end
  def watch_tv
    puts "Nothing on tv"
  end
end
my_room = Bedroom.new("Jack", white)
my_room.bed #=> 1
my_room.bed = 2 #=> 2
my_room.sleep #=> zzzZzzzZzz
{% endhighlight %}