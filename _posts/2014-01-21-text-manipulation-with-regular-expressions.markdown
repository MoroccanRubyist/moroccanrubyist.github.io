---
layout: post
title:  Text manipulation with Regular Expressions
date:   2014-01-21 05:00:00
author: Youssef Kababe
github: YoussefKababe
categories: sessions ruby
thumbnail: regex.png
description: Regular Expressions give you more power when manipulating text and strings. This tutorial is an
  introduction to the basics of using Regular Expressions in Ruby.
youtube: mmNEEC_s7j8
---

### What you'll learn?
* What are Regular Expressions?
* Matching strings agains Regular Expressions
* Basics of string manipulation using Regulat Expressions

***

### Code from the tutorial

{% highlight ruby %}
# Username validation
# # # # # # # # # # #

def validate_username uname
  reg = /\A[a-z0-9_-]{4,}\z/i
  if uname =~ reg
    return "Username is valid!"
  else
    return "Username is not valid!"
  end
end

puts validate_username "Youssef"
{% endhighlight %}

{% highlight ruby %}
# Palindrome verification
# # # # # # # # # # # # #

def palindrome? str
  arr = str.downcase.scan(/\w/)
  arr == arr.reverse
end

puts palindrome? "Never a foot too far, even"
{% endhighlight %}

***
### Resources
![Rubular](/images/regexp/rubular.png)
[Rubular](http://www.rubular.com/) is a handy tool that you can use to test your
Regular Expressions before using them in your code.
***
