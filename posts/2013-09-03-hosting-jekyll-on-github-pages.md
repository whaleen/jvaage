---
title:  "Hosting Jekyll On GitHub Pages"
date:   2013-09-03 13:00:21
tags:
  - jekyll
  - github pages
layout: layouts/post.njk
---

After [Setting Up Jekyll Locally](#), it's now time to create a Git repository. We will also be using GitHub to host the remote repositry. A Git repository will serve us in two ways.

1. Because it is wise to have version control and GitHub is great for that.
2. A Git repository stored at GitHub can be generated into hosted website complete with [a custom domain name](#).


Move into the Jekyll project directory

{% highlight bash %}
~ $ cd joshuavaage.com
{% endhighlight %}


Create a Git repository for the Jekyll project.

{% highlight bash %}
~ $ git init
{% endhighlight %}

[Create a remote repository](https://github.com/new) at GitHub which we will push our local repo up to..


[https://help.github.com/articles/using-jekyll-with-pages](https://help.github.com/articles/using-jekyll-with-pages)
