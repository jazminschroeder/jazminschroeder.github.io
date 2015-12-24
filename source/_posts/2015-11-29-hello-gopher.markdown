---
layout: post
title: "Hello Gopher"
date: 2015-11-29 12:33:02 -0600
categories: golang
---

#### Download and install
Download [Golang](https://golang.org/dl/) and install it.

#### Create your workspace
{% highlight ruby %}
$ mkdir goprojects
$ export GOPATH=$HOME/goprojects
$ cd goprojects
$ mkdir -p src/github.com/jazminschroeder
$ cd src/github.com/jazminschroeder
{% endhighlight %}

#### Creating a project
{% highlight ruby %}
$ mkdir hello_gopher
$ cd hello_gopher
$ vim hello_gopher.go
 
 # Hello gopher 
 package main
 import "fmt"

 func main() {
  fmt.Println("Hello gopher!!!")
 }
{% endhighlight %}

#### Go install
{% highlight ruby %}
 $ go install
{% endhighlight %}


#### Say hello gopher!
{% highlight ruby %}
$ ~/goprojects/bin/hello_gopher
$ Hello gopher!!!

{% endhighlight %}
