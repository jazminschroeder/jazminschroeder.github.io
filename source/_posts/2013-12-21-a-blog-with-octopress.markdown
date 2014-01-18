---
layout: post
title: "Starting with a blog with octopress"
date: 2013-12-21 18:55:52 -0600
comments: true
categories:
---

I decided to start a new technical blog, the main purpose is to keep a record of things I have learned which could potentially help others. My first obvious choice was Wordpress after all is the number one bloging engine out there but somebody mentioned Octopress and so here we are.


Octopress is a framework for Jekyll the blog static site generator powering Github Pages. If you enjoy working with the console then Octopress will feel very comfortable. There are a lot of resources out there to get you started with <a href="http://jekyllrb.com/" target="_blank">Jekyll</a> and github pages,  <a href="http://octopress.org" target="_blank">Octopress</a> just makes it dead simple to get up and running in no time and there are a lot of themes and plugins ready to use to make your blog your own.

Use your favorite editor, commit to Github, deploy with a simple rake task and host your blog at Github for free. How can you go wrong with that?
<!-- more -->

#### Everything you need is one rake away

{% highlight ruby %}
rake clean                     # Clean out caches: .pygments-cache, .gist-c...
rake copydot[source,dest]      # copy dot files for deployment
rake deploy                    # Default deploy task
rake gen_deploy                # Generate website and deploy
rake generate                  # Generate jekyll site
rake install[theme]            # Initial setup for Octopress: copies the de...
rake integrate                 # Move all stashed posts back into the posts...
rake isolate[filename]         # Move all other posts than the one currentl...
rake list                      # list tasks
rake new_page[filename]        # Create a new page in source/(filename)/ind...
rake new_post[title]           # Begin a new post in source/_posts
rake preview                   # preview the site in a web browser
rake push                      # deploy public directory to github pages
rake rsync                     # Deploy website via rsync
rake set_root_dir[dir]         # Update configurations to support publishin...
rake setup_github_pages[repo]  # Set up _deploy folder and deploy branch fo...
rake update_source[theme]      # Move source to source.old, install source ...
rake update_style[theme]       # Move sass to sass.old, install sass theme ...
rake watch                     # Watch the site and regenerate when it changes
{% endhighlight %}
