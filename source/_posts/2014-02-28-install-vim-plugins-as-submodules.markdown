---
layout: post
title: "Install vim plugins as submodules"
date: 2014-01-28 23:24:38 -0600
comments: true
categories: vim
---

### Step 1
{% highlight ruby %}
$ git submodule add http://https://github.com/tpope/vim-surround bundle/surround
{% endhighlight %}

### Step 2
{% highlight ruby %}
$ git submodule init
$ git submodule update
{% endhighlight %}
