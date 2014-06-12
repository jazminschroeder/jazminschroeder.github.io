---
layout: post
title: "Using tags with cucumber"
date: 2014-06-11 22:32:53 -0500
comments: true
categories: cucumber
---

{% highlight ruby %}
@mytag
Scenario:

$ cucumber --tags @mytag

{% endhighlight%}

