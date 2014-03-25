---
layout: post
title: "Neo4J change default remote shell port"
date: 2014-03-22 22:34:11 -0500
comments: true
categories: neo4j
---

Neo4j remote shell port defaults to 1337. How to change it?

{% highlight ruby linenos=table %}
# /usr/local/neo4j-server/conf/neo4j.properties
remote_shell_port = 1338
{% endhighlight %}
