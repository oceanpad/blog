---
title: Front end 3 steps
date: 2016-05-11 10:03:53
tags:
---
what is npm :
npm is the package manager for JavaScript. Find, share, and reuse packages of code from hundreds of thousands of developers — and assemble them in powerful new ways.

<!--more-->
#### npm 3 things need to remember
# 1. npm init
```
npm init
```
npm will take charge all the files under this directory.
After this action, you will found there have a [package.json] file appear.
![picture](/resource/npm3steps/1.png)

# 2. npm install
eg. install jquery:
```
npm install jquery --save
```
[jquery] is the package name
After this step, a new jquery folder will appear under node-model. 
And package.json's dependencies will add a jquery automqtically.
![picture](/resource/npm3steps/2.png)

# 3. npm run
run task
```
npm run
```
![picture](/resource/npm3steps/3.png)

