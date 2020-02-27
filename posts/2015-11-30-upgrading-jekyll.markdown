---
layout: post
title:  "Ugrading Jekyll from v2.5.3 to v3x"
date:   2015-11-30 18:58:32
tags:
- jekyll
- ruby
- gem
description: The watching-paint-dry version of a Jekyll upgrade walkthrough post.
layout: layouts/post.njk
---

I am currently running 2.5.3. Official Jekyll docs provide the resource [Upgrading from 2.x to 3.x](http://jekyllrb.com/docs/upgrading/2-to-3/), which outlines some of the known changes I will need to make to older Jekyll sites. I will document any useful findings as I upgrade.

### First, update Jekyll gem.

`sudo gem update jekyll`

> Updating installed gems  
Updating jekyll
Fetching: jekyll-3.0.1.gem (100%)^[[C  
Successfully installed jekyll-3.0.1  
Parsing documentation for jekyll-3.0.1  
Installing ri documentation for jekyll-3.0.1  
Installing darkfish documentation for jekyll-3.0.1  
Done installing documentation for jekyll after 9 seconds  
Parsing documentation for jekyll-3.0.1  
Done installing documentation for jekyll after 2 seconds  
Gems updated: jekyll  

That was nice. Now, I'll run this site locally and see what I'll need to address.

`$ cd jvaage && jekyll serve --watch`

> Liquid Exception: Liquid syntax error: Unknown tag 'gist'

This was expected as the _jekyll-gist_ gem is listed as no longer included.

## Concerning Dependencies

> We dropped a number of dependencies the Core Team felt were optional. As such, in 3.0, they must be explicitly installed and included if you use any of the features. - **Jekyll Docs:** [Dropped Dependencies](http://jekyllrb.com/docs/upgrading/2-to-3/#dropped-dependencies).

Explicitly install _some formally included_ plugins. Easy enough.

`gem install jekyll-gist.rb`

Another former dependecy, Pygments, provided syntax highlighting. Now, Rouge is the Jekyll default. Note: the `highlight` tag will still work, however you should read about [what changes](http://jekyllrb.com/docs/upgrading/2-to-3/#syntax-highlighter-changed) might affect your usage of that tag. If you are not adverse to explicitly installing gems and want to continue using Pygments:

`gem install pygments.rb`

That is all. I will update this post with any findings I make running the several other Jekyll sites I manage.
