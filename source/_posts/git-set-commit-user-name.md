---
title: git set commit user profile
date: 2016-05-12 10:53:35
tags:
---
git set commit history user.name and user.email
<!--more-->
# reset git history user
```
git filter-branch -f --env-filter "
  GIT_AUTHOR_NAME='oceanpad'
  GIT_AUTHOR_EMAIL='zhy20090912@gmail.com'
  GIT_COMMITTER_NAME='oceanpad'
  GIT_COMMITTER_EMAIL='zhy20090912@gmail.com'
" HEAD
```

# set globle user profile 
```
git config --globle user.name "oceanpad"
git config --globle user.email "zhy20090912@gmail.com"
```

# set local user profile 
under this directory's set file
```
git config --globle user.name "oceanpad"
git config --globle user.email "zhy20090912@gmail.com"
```
