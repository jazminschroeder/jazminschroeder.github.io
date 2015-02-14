---
layout: post
title: "dyld: Library not loaded: /usr/local/lib/libevent-2.0.5.dylib"
date: 2015-02-14 12:08:42 -0600
comments: true
categories: tmux
---

<h3>Problems with tmux?</h3>

{% highlight ruby %}
$ tmux
dyld: Library not loaded: /usr/local/lib/libevent-2.0.5.dylib

# Install libevent
$ brew install libevent
Warning: libevent-2.0.21 already installed

# Already intalled. Where is it?
$brew link libevent
Warning: Already linked: /usr/local/Cellar/libevent/2.0.21
To relink: brew unlink libevent && brew link libevent

# Relink it
$brew unlink libevent && brew link libevent
{% endhighlight%}
