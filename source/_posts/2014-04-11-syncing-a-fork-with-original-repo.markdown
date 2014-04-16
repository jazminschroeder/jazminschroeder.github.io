---
layout: post
title: "Syncing a fork"
date: 2014-04-11 10:59:03 -0500
comments: true
categories: git, github
---

{% highlight ruby %}
#Set a new remote for the orinal repository
$ git remote add upstream git@github.com:jazminschroeder/repo.git

#fetch upstream's branches
$ git fetch upstream

#merge upstream
$ git merge upstream/master

{% endhighlight%}

