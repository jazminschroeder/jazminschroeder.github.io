---
layout: post
title: "Cucumber Scenario Outlines"
date: 2014-03-06 15:02:41 -0600
comments: true
categories: cucumber
---

{% highlight ruby linenos=table %}
Scenario Outline: Table example
 Given I have an "<option>"
 Then I should see "<result>"

 Examples:
   | option   | result   |
   | option 1 | result 1 |
   | option 2 | result 2 |
{% endhighlight %}
