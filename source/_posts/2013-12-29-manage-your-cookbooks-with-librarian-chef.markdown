---
layout: post
title: "Manage your cookbooks with librarian-chef"
date: 2013-12-29 22:17:59 -0600
comments: true
categories: chef
---

<a href="https://github.com/applicationsonline/librarian-chef" target="_blank">librarian-chef</a> is like a bundler for cookbooks. Manage your cookbooks and dependencies in a single file.

<h3>Here is how</h3>

{% highlight ruby linenos=table %}
$ gem install librarian-chef
$ librarian-chef init
# edit the newly created Cheffile to add your cookbooks
$ librarian-chef install
{% endhighlight %}

Cookboks listed in the Cheffile will be downloaded to the cookbooks folder, you will also noticed a Cheffile.lock is created locking the versions.

<!-- more -->

<h3>Here is an example:</h3>
{% highlight text linenos=table %}
#!/usr/bin/env ruby
#^syntax detection

site 'http://community.opscode.com/api/v1'
cookbook 'apt'
cookbook 'git'
cookbook 'build-essential'
cookbook 'tmux'

# Include cookbooks from github 
cookbook 'ruby_build', 
          :git => 'https://github.com/fnichol/chef-ruby_build.git'
cookbook 'rbenv',
          :git => 'https://github.com/fnichol/chef-rbenv.git',
          :ref => 'v0.7.2'

{% endhighlight %}



