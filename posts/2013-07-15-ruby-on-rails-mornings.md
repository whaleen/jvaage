---
layout: post
title:  "Rails Mornings"
tags:
- rails
- ruby
date:   2013-08-05 13:00:21
layout: layouts/post.njk
---

I jumped straight into Ruby 2 and Rails 4. I should have held back. Now I realize the importance of using RVM. I'm running Jekyll which wants Rails 1.9.3 as of now and I'm just learning Rails and many of the so called application templates are built to run on Rails 3.


Toggling Ruby versions before working on a new or another project. I understand there are probably ways to set versions to automatically be used on a project by project basis but I want to start building something before I get too crazy setting everything up. Plus, I'm learning about how this all works as a result of manually taking care of these specific things I am just beginning to understand. Reinforcement.


### Setting @--default@ Ruby version

{% highlight bash %}
$ rvm use 1.9.3 --default
{% endhighlight %}

{% highlight bash %}
$ rvm use 2.0.0 --default
{% endhighlight %}

After commanding my computer with either of those previous commands I can do

{% highlight bash %}
$ ruby -v
{% endhighlight %}

and it will tell me which version is currently running in my terminal and any other new terminal windows as  I've set the new default. Previously opened terminal windows will retain their defaults that have been set. This is useful to me as I'll first get Jekyll up and serving in terminal window with Ruby 1.9.3 as the --default and then I'll open up another Terminal window and….


And don't forget gemsets: http://www.microtuts.com/install-ruby-on-rails-3-2-with-rvm/


Create a Gem Set:

$ rvm gemset create gemsetname

Make it current default:

$ rvm use 1.9.3@gemsetname --default

Add Rails version we want in this Gem Set:

$ gem install rails --version 3.2.0

or

$ gem install rails --version 4.0.0

or for the latest

$ gem install rails







Getting into the gemset I need:

$ rvm use ruby-1.9.3-p448@rails32_openvintage --default





in my gemset to get proper old rails version in the gemset:

$ gem install rails --version '~> 3.2.0'
