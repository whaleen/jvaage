---
title: Making a GitHub Repository Collection in 11ty
description: 'Importing GitHub repositories into 11ty.'
date: 2020-02-26T08:00:00.000+00:00
tags:
- 11ty
- github
layout: layouts/post.njk

---

Make a JSON file listing all my GitHub repositories and make a collection out of them.




1. Add a script to the package.json file. Replace 'whaleen' with any username.

``` javascript
"gh-repos": "curl https://api.github.com/users/whaleen/repos -o _data/repos.json"
```

2. Create the file in 11ty's _data folder called repos.json.

``` shell
npm run gh-repos
```

3. Consume the data

``` yaml
---
layout: layouts/base.njk
pagination:
  data: repos
  size: 1
  alias: repo
permalink: repo/{{ repo.id }}/index.html
---
```

!!! this code block is trying to render my curly tags
```
<h1>{{ repo.name }}</h1>
<h2>@{{ repo.owner.login }}</h2>
<p>
  {{ repo.description }}
</p>
Repo: <a class="h1" href="{{ repo.url }}">{{ repo.url }}</a>

<h3>Clone Repo</h3>
<pre>git clone  {{ repo.clone_url }}</pre>

Stargazers {{ repo.stargazers_count }} |
Watchers {{ repo.watchers_count }} |
Language: {{ repo.language }}

```

resume writing this when i figure that out. 
