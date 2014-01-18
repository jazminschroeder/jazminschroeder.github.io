---
layout: post
title: "Berkshelf a vagrant plugin"
date: 2014-01-18 16:31:03 -0600
comments: true
categories: vagrant, chef
---

<a href="http://berkshelf.com/" target="_blank">Berkshelf</a> is a bundler-like dependency manger for Chef cookbook. <a href="https://github.com/berkshelf/vagrant-berkshelf">vagrant-berkshelf</a> is a Vagrant plugin to add Berkshelf integration to Chef provisioners to avoid the need to install cookbooks locally and have everything ready when you bring vagrant up.

### How to use?
Install vagrant-berkshelf

<!-- more -->

{% highlight ruby %}
$ vagrant plugin install vagrant-berkshelf
{% endhighlight %}

Enable it in Vagrantfile
{% highlight ruby %}
Vagrant.configure("2") do |config|
  ...
  config.berkshelf.enabled = true
  ...
end
{% endhighlight %}

Generate a Berksfile in the root of your project

{% highlight ruby %}
site :opscode
cookbook 'apt'
cookbook 'build-essential'

cookbook 'ruby_build', git: 'https://github.com/fnichol/chef-ruby_build.git'
cookbook 'rbenv', git: 'https://github.com/fnichol/chef-rbenv.git'

cookbook 'vim', path: './cookbooks/vim'

{% endhighlight %}

### That's it! vagrant up  ###
