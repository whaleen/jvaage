---
layout: post
title: "Bible Text HTML"
excerpt:
tags:
- microformats
- bibleref
image:
  feature:
date: 2015-03-24T03:16:17-07:00
layout: layouts/post.njk
---

### Microformat

Complete text of two Bible verses where the underlying HTML markup describes which bible version, book, chapter, and verse using class names, all within the proposed _bibleref_ microformatted div.

{% highlight html %}
<div class="esv bibleref" lang="en">
<h2><span class="book">1 Peter</span>
	<span class="chapter">1</span>:
	<span class="verse">1-2</span>
</h2>

<p class="1 2">Peter, an apostle of Jesus Christ, To God’s elect, exiles scattered throughout the provinces of Pontus, Galatia, Cappadocia, Asia and Bithynia, 2 who have been chosen according to the foreknowledge of God the Father, through the sanctifying work of the Spirit, to be obedient to Jesus Christ and sprinkled with his blood: Grace and peace be yours in abundance.</p>
</div>
{% endhighlight %}

These two verses formatted as such can now be parsed by a machine to produce the resulting answer: **1 Peter 1:1,2**


<div class="esv bibleref" lang="en">
<h2><span class="book">1 Peter</span>
	<span class="chapter">1</span>:
	<span class="verse">1-2</span>
</h2>

<p class="1 2">Peter, an apostle of Jesus Christ, To God’s elect, exiles scattered throughout the provinces of Pontus, Galatia, Cappadocia, Asia and Bithynia, 2 who have been chosen according to the foreknowledge of God the Father, through the sanctifying work of the Spirit, to be obedient to Jesus Christ and sprinkled with his blood: Grace and peace be yours in abundance.</p>
</div>
