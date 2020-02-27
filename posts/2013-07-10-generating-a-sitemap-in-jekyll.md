---
title: Jekyll thing
tags:
  - jekyll
  - ruby
  - plugin
layout: layouts/post.njk
---

### Requires a Plugin

[sitemap_generator.rb](https://github.com/whaleen/jekyll-plugins/blob/master/sitemap_generator.rb) by [Michael Levin](https://github.com/kinnetica)

### Steps to Take

1. Add a new folder to the project named ``_plugins/`` alongside ``_site/``.
2. Add [sitemap_generator.rb](https://github.com/whaleen/jekyll-plugins/blob/master/sitemap_generator.rb) to it.
3. Change ``MY_URL``  in sitemap_generator.rb to reflect your domain name.

Run Jekyll to re-generate your site:

{% highlight bash %}
~ $ jekyll --server
{% endhighlight %}

In order to make the Sitemap truly useful for different cases, more configuration is possible. Read about that in the plugin's [README.md](https://github.com/kinnetica/jekyll-plugins/blob/master/README.md).

### For Example:

> Change the ``PAGES_INCLUDE_POSTS`` list to include any pages that are looping through your posts (e.g. "index.html", "archive.html", etc.). This will ensure that right after you make a new post, the last modified date will be updated to reflect the new post.

-------------------------------------

### General Plugin Resources

- [Jekyll Plugins Documentation](http://jekyllrb.com/docs/plugins/)
- [Getting Started with Jekyll Plugins
](http://tech.pro/tutorial/1299/getting-started-with-jekyll-plugins)
