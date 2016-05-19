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

* issue
[issue](http://stackoverflow.com/questions/37169378/in-facebook-open-source-project-fbctf-error-in-starting-the-application)

### 2016-05-14
Today is saturday, I play my facebook ctf at home. And at last I foound ctf game's enter.
Fbctf is using nginx as it's http server. The default port is 80, and I don't know it before, so I coundn't found the enter.
#### fbctf welcome apge
![welcome home page](/resource/fbctf/welcome.png)

#### login page
![login page](/resource/fbctf/login.png)

#### password
```
default user is admin and password is provided code when you start the server.
```
![password](/resource/fbctf/admin_password.png)

#### game home page
![game home](/resource/fbctf/game_home.png)

#### server game admin 
![server admin](/resource/fbctf/server_admin.png)

#### begin game 
![begin game](/resource/fbctf/begin_game.png)

#### world map 
![world map](/resource/fbctf/world_map.png)

#### all dashboard 
![all dashboard](/resource/fbctf/all_dashboard.png)

#### score board 
![score board](/resource/fbctf/score_board.png)

=====================================
=====================================
=====================================
=====================================

```
At last, I can play fbctf well. Super good mode.

```
