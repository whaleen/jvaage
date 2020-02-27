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
    [build]  

      command = 'curl https://api.github.com/users/whaleen/repos -o repos.json; jekyll build'