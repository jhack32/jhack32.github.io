---
layout: post
title:  "Arrays and Hashes"
date:   2015-10-04
categories: arrays hashes
---

# What is an array/hash?
`Arrays` can be thought of like an ordered list. It has things on the list and is numbered. An array starts from 0. The first item on an array has an index-number of 0. It could also have an array within an array. There could be sub-arrays.
`Hashes` on the other hand contain a key and a value. Unlike arrays, it's not number indexed. You do not find a value by trying to enter a number unless the key is a number. If you want to get to an item, you can call the hash along with the key. It may look something like

{% highlight ruby %}
hash {
    :keyone => 1,
    :keytwo => 2
}
hash[:keyone] #=> 1

{% endhighlight %}

#Comparison
Arrays are used without a key. It doesn't have a key and a value like a hash. Below example shows an array being created with strings. Then it's calling for the string "zero". You can also retrieve the last item by doing `array[-1]` which will get the string "two" or `array[-2] => "one"`.

{% highlight ruby %}
array = ["zero", "one", "two"]
array[0] #=> "zero"
{% endhighlight %}

Arrays are called by using an index number like the example above. Hashes on the other hand, are called by using `keys`. They can have multiple arrays within one array. We cannot have multiple hashes in one hash though. That's what the key's are for. The keys are similar to creating sub-categories. Hashes also return a nil value when the key doesn't exist.

{% highlight ruby %}
array = ["zero", ["second-array"], ["third"]]
{% endhighlight %}

Arrays and hashes have their individual uses. Hashes would be used to store things like "person has a dog" or "dog is 2 years old". They require a unique key. The key can't be reused in the same hash. Arrays can store information about a certain category like `dogs = ["pitbull", "beagle", "golden retriever"]`. They don't have a key but retrieved by using an index number starting from 0.