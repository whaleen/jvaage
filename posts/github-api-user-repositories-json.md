---
title: 'GitHub API: User Repositories JSON'
description: 'Testing on netlify to create repos.json file on build of any static
  site. '
date: 2020-02-27T08:00:00Z
tags:
- api
- sssg
- jekyll
- netlify
- github
layout: layouts/post.njk

---
A basic `jekyll build` command including a call to the GitHub API. The response is output to a _repos.json_ file

``` shell
curl https://api.github.com/users/whaleen/repos -o repos.json; jekyll build
```


In a 11ty site I have hosted on netlify, this in my `netlify.toml` file:

``` toml
    [build]
      command = 'curl https://api.github.com/users/whaleen/repos -o repos.json; jekyll build'
```      

Netlify will run that build command whenever a deploy is triggered.
