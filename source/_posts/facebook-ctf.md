---
title: facebook ctf
date: 2016-05-12 23:22:46
tags:
---
Facebook CTF had become Open souce today.
![fabook ctf](/resource/fbctf/1.gif)
<!--more-->
The Facebook CTF is a platform to host Jeopardy and “King of the Hill” style Capture the Flag competitions.

### Production
```
The target system needs to be Ubuntu 14.04. Run the following commands:

sudo apt-get install git
git clone https://github.com/facebook/fbctf
cd fbctf
./extra/provision.sh prod `pwd`
```

### Development
```
git clone https://github.com/facebook/fbctf
cd fbctf
vagrant up
```
* facebook ctf init commit on [Jan 30 2016]
![facebook ctf inin commit](/resource/fbctf/2.png)

### issue
Sometimes you can't install vagrant by command line, so you need download form net and install it:
* [download URL:](https://www.vagrantup.com/downloads.html)
![can't download](/resource/fbctf/3.png)
* sometimes can't install by command line.
![can't download](/resource/fbctf/4.png)
