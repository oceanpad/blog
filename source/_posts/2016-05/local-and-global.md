---
title: local and global
date: 2016-05-14 13:11:14
tags:
---
The different between [global] and [local]
Only for linux.
<!--more-->
Recently I use github usually, I have two github account,
One is for company, and one is for mysely use only. When I
push comtents at company, I found that github's result author
is my company's emial address. But I really want to change it
to my own email.
I had search so so many, and set my git config files for times.
But I can't change result Author. 
### I use code check git user and email under my own repository folder.
```
git config user.name
git config user.email
```
It show that git user name and email are all company's.

But When I use the same command to show git user under company's repository.It show the same user and email.
So I search git user set. I found that thera have global and local parameters when you set linux config ussally.
Probably, I set global config when I use git at the first time. Like this:
```
git config --global user.name <company user name>
git config --global user.email <company user email>
```

### So I change my git user set to local set under my own repository folder. Like this :
```
git config --local user.name "oceanpad"
git config --local user.email "zhy20090912@gmail.com"

OR REMOVE --local paraameter

git config  user.name "oceanpad"
git config  user.email "zhy20090912@gmail.com"
```

After setting these, when you check your git user under your repository one mmore time, you will found that you set you git user only under this folder. The other repositoried folder's git user still are globle set git user.

* Like This :
#### set global user
![global git user set](/resource/globle_local/1.png)
#### set local user
![local git user set](/resource/globle_local/2.png)
