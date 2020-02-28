---
title: Making a GitHub Repository Collection in 11ty
description: ''
date: 
tags:
- 11ty
- github
layout: layouts/post.njk

---
\---

layout: layouts/post.njk

title: Repos

templateClass: tmpl-post

eleventyNavigation:

  key: Repos

\---

<ol>

{% for repo in repos -%}

<li>

<a href="/repo/{{ repo.id }}">{{ repo.name }}</a> - {{ repo.stars }}

</li>

{% endfor -%}

</ol>