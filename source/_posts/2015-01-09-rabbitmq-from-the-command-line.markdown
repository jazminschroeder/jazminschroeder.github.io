---
layout: post
title: "RabbitMQ from the command line"
date: 2015-01-09 13:34:34 -0600
comments: true
categories: rabbitmq command line
---

<a href="http://www.rabbitmq.com/man/rabbitmqctl.1.man.html">rabbitmqctl</a>

<h3>List queues messages and consumers</h3>
{% highlight ruby %}
$ sudo rabbitmqctl list_queues name messages consumers

Listing queues ...
test.two.queue  0       0
test.one.queue     0       0

{% endhighlight%}

<h3>List exchanges</h3>
{% highlight ruby %}
$ sudo rabbitmqctl list_exchanges
{% endhighlight%}
