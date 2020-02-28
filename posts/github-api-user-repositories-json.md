---
title: 'GitHub API: User Repositories JSON'
description: 'Testing on netlify to create repos.json file on build of any static
  site. '
date: 2020-02-27T08:00:00.000+00:00
tags:
- api
- sssg
- jekyll
- netlify
- github
layout: layouts/post.njk

---
A call to the GitHub API. The response is output to a _repos.json_ file

``` shell
curl https://api.github.com/users/whaleen/repos -o repos.json;
```

Test the output received at: [https://api.github.com/users/whaleen/repos](https://api.github.com/users/whaleen/repos)

## Jekyll Use Case

In a Jekyll site I have hosted on netlify, this in my `netlify.toml` file:

``` toml
[build]
  command = 'curl https://api.github.com/users/whaleen/repos -o _data/repos.json; jekyll build'
```      

Netlify will run that build command whenever a deploy is triggered. Netlify respects your netlify.toml file.

## 11ty Use Case

Same as with Jekyll I will put the repos.json into a _data file.

Add script to package.json:

```javascript
"scripts": {
  "build": "eleventy",
  "watch": "eleventy --watch",
  "serve": "eleventy --serve",
  "debug": "DEBUG=* eleventy",
  "comment": "Script below, gh-repos, gets repos and puts in _data dir for consumption by 11ty or Jekyll",
  "gh-repos": "curl https://api.github.com/users/whaleen/repos -o _data/repos.json"

}
```

Run it:

```shell
npm run gh-repos
```

[Making a Repo Collection in 11ty](#)
