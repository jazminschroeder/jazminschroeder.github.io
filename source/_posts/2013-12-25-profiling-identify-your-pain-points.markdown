---
layout: post
title: "RubyProf: Identify your pain points"
date: 2013-12-25 17:28:16 -0600
comments: true
categories: ruby
---

We all have been there: the site worked great in development but not so great in Production. Time to optimize! but... How to know what to optimize?

<a href="https://github.com/ruby-prof/ruby-prof" target="_blank">RubyProf</a> is a fast code profiler for Ruby which helps you find pain points in your code by providing different measure parameters including call times, memory usage and object applications.
<!-- more -->

<h3>Show me the code!</h3>
{% highlight ruby linenos=table %}
require 'ruby-prof'
RubyProf.start

1.upto(100) do |number|
  if number % 5 == 0
    p 'Divider'
  else
    p number
  end
end

result = RubyProf.stop
printer = RubyProf::MultiPrinter.new(result)
printer.print(:path => ".", :profile => "profile")
{% endhighlight %}

Now take a pic at the profile flat report.

{% highlight txt %}
Thread ID: 70113135123160
Fiber ID: 70113151681380
Total: 0.000937
Sort by: self_time

 %self      total      self      wait     child     calls  name
 41.73      0.001     0.000     0.000     0.000      100   Kernel#p
 24.87      0.001     0.000     0.000     0.001        1   Integer#upto
 10.99      0.000     0.000     0.000     0.000       80   Kernel#inspect
 10.46      0.001     0.000     0.000     0.001        1   Global#[No method]
 7.90      0.000     0.000     0.000     0.000       80   Fixnum#to_s
 4.06      0.000     0.000     0.000     0.000       20   String#inspect

         * indicates recursively called methods
{% endhighlight %}

{% img left /images/call_tree.png 350 350 'image' 'images' %}
{% img right /images/profile_graph.png 350 350 'image' 'images' %}


