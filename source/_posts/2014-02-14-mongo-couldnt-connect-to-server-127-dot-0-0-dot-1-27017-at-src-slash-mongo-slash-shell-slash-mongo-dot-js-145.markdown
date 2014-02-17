---
layout: post
title: "Mongo: couldn't connect to server 127.0.0.1:27017 at src/mongo/shell/mongo.js:145"
date: 2014-02-14 14:19:40 -0600
comments: true
categories: 
---

Problems with mongo lock?


{% highlight ruby %}
$ sudo rm /var/lib/mongodb/mongod.lock
$ sudo service mongodb restart
{% endhighlight %}
