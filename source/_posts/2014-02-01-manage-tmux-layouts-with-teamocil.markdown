---
layout: post
title: "Manage Tmux layouts with teamocil"
date: 2014-02-01 12:47:36 -0600
comments: true
categories: tmux
---

Starting a tmux session? Open windows, panes, start services and more all with one  command. Meet  <a href="https://github.com/remiprev/teamocil" target="_blank">Teamocil</a> 

### How to install teamocil? ###

{% highlight ruby %}
$ gem install teamocil
{% endhighlight %}

<!-- more -->
### How to create a teamocil layout? ###

<script src="https://gist.github.com/jazminschroeder/8757578.js"></script>

### How to use my new layout? ###

{% highlight ruby %}
$ tmux
$ teamocil my_layout --here
{% endhighlight %}



### And... ###

{% img center /images/teamocil_my_layout.png  'image' 'images' %}


