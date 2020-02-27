---
layout: post
title: "Jekyll manifest.json"
modified:
categories: jekyll
excerpt:
tags: [jekyll, json]
date: 2015-11-22 12:07:15
layout: layouts/post.njk
---

Prompted to create this for present and future Jekyll projects after seeing [a link on adactio.com](https://adactio.com/links/9839) to
this [Manifest Generator](http://brucelawson.github.io/manifest/) which then led me to find a good reason (article), [Installable Web Apps](https://dev.opera.com/articles/installable-web-apps/), for such thing.

### _config.yml

{% highlight yaml %}

# Manifest settings (Used to make manifest.json)
# Edit manifest.json directly concerning icon information
# A sample icon is in the /img directory and manifest.json references that icon.
manifest_name: Web App Full Name
manifest_short_name: Short Name # Appears in "Add to home screen" dialogues and may have other importance also
manifest_lang: en
manifest_background_color: white
manifest_short_name:
manifest_display: standalone

{% endhighlight %}



### manifest.json

{% highlight json %}

---
permalink: manifest.json
---

{
  "lang": "{{ site.manifest_lang }}",
  "background_color": "#{{ site.manifest_background_color }}",
  "name": "{{ site.manifest_name }}",
  "short_name": "{{ site.manifest_short_name }}",
  "display": "{{ site.manifest_display}}",
  "icons": [
    {
      "src": "img/144X144-icon.png",
      "sizes": "144x144",
      "type": "image/png"
    }
  ]
}

{% endhighlight %}

See [Github repository](https://github.com/whaleen/Jekyll-manifest.json).
