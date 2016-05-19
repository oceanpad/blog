---
title: upgrade your nodejs
date: 2016-05-18 05:15:34
tags:
---
Node.js is being actively developed, and the latest stable version frequently changes. From time to time you will find a module that doesn’t work with your current version of Node and says that you need to upgrade.
<!--more-->

Fortunately there is a very easy way of managing your node version, using the Node binary manager module [n](https://github.com/tj/n).

# Check your current version of Node.
```
$ node -v v0.6.12
```
# Clear your npm cache
```
$ sudo npm cache clean -f  
```
# Install ‘n’
```
$ sudo npm install -g n  
```
# Upgrade to a later version (this step can take a while) You can specify a particular version like so:
```
$ sudo n 0.8.11  
```
Or you can just tell the manager to install the latest stable version like so:
```
$ sudo n stable  
```
# Check the running version of Node to verify that it has worked:
```
$ node -v v0.8.11
```
If the version doesn’t number output in step 5 isn’t what you were expecting, you may need to reboot.
