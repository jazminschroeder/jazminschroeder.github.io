---
layout: post
title: "Ruby and Statsd"
date: 2015-04-16 15:40:44 -0500
comments: true
categories: ruby statsd graphite
---


<h3>Graph everything</h3>

[https://github.com/reinh/statsd](Using statsd-ruby gem)

{% highlight ruby %}
require 'statsd'

statsd = Statsd.new('localhost', 9125)
statsd.namespace="some.namespace"

#Sending data
statsd.increment 'foo.bar'
{% endhighlight%}
