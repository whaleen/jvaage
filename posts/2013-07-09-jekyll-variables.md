---
date:   2013-07-09 13:00:21
tags:
  - jekyll
  - variables
layout: layouts/post.njk
---


Variables can be set in the ``_config.yml`` file located in the project root.

> Jekyll does not parse changes to  ``_config.yml`` in watch mode, you must restart Jekyll to see changes to variables. - [http://jekyllrb.com/docs/variables/](http://jekyllrb.com/docs/variables/)



And [jekylls-auto-doesnt-work](http://stackoverflow.com/questions/15591000/jekylls-auto-doesnt-work)

## Restart Jekyll?

Yes. By quitting, and then starting again. ``Ctrl-C`` in your terminal window running Jekkyl to stop the Jekyll server. Now fire it up again:

{% highlight bash %}
jekyll serve --watch
{% endhighlight %}
