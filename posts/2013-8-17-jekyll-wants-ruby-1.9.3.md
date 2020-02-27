---
layout: post
title:  "Jekyll Wants Ruby 1.9.3"
date:   2013-08-17 08:37:21
layout: layouts/post.njk
---

Different Ruby versions can be run for different projects on a folder by folder basis. Take these folders and their suggested Ruby version as an example:

- /my-jekyll-site _(Ruby 1.9.3)_
- /my-rails-4-app _(Ruby 2.0.0)_

Let's start with Jekyll:

{% highlight bash %}
$ cd my-jekyll-site
{% endhighlight %}

Set `--default` Ruby version

{% highlight bash %}
$ rvm use 1.9.3 --default
{% endhighlight %}


Create the Gem Set that Jekyll will use:

{% highlight bash %}
$ rvm gemset create jekyllgemsetname
{% endhighlight %}

Make it default for the Jekyll project directory:

{% highlight bash %}
$ rvm use 1.9.3@jekyllgemsetname --default
{% endhighlight %}
