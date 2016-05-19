---
title: linux share folder
date: 2016-05-12 04:22:32
tags:
---
Sometimes you want to share files between hosts and guest, 
So you need use virtualbox's shared folder feature.
<!--more-->
### install iso file
```
sudo apt-get install virtualbox-guest-additions-iso
```

### add share folder
* set share folder at virtualbox host client
![set share foler at client](/resource/share_folder/1.png)

### install guest additions ios
make sure you had installed virtualbox-guest-additions-iso, if not install it by this:
```
sudo apt-get install virtualbox-guest-additions-iso
```

### add user to share folder 
Access to auto-mounted shared folders is only granted to the user group vboxsf, which is created by the VirtualBox Guest Additions installer. Hence guest users have to be member of that group to have read/write access or to have read-only access in case the folder is not mapped writable.
```
sudo adduser [your_user_name] vboxsf
```
after all of this, well done!

reference: [Can't access shared folder in VBox](http://ubuntuforums.org/showthread.php?t=2075432)
