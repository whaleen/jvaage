---
layout: post
title:  "Setting up Jekyll Locally"
date:   2013-07-09 13:00:21
categories: jekyll
tags:
- jekyll
- ruby
- os x
layout: layouts/post.njk
---


Install Jekyll

{% highlight bash %}
~ $ gem install jekyll
{% endhighlight %}


Create new Jekyll Project

{% highlight bash %}
~ $ jekyll new jvaage
{% endhighlight %}

Now I have the new directory **/jvaage**

Now move into that directory:

{% highlight bash %}
~ $ cd jvaage
{% endhighlight %}

Now serve Jekyll site for local viewing via [http://localhost:4000](http://localhost:4000):

{% highlight bash %}
$ jekyll serve --watch
{% endhighlight %}
