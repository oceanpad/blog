---
title: cordova run config
date: 2016-05-17 11:03:33
tags:
---
If you want to use make web app can run in many platforms like ios, andorid and so on, you can learn cordova.
Write one time use html, css, javascript, run everywhere.
React.js is very popular recently, you can use js framework to make your web app better and better.
[cordova cordova homePage](https://cordova.apache.org/)

![cordova](/resource/cordova/cordova.jpg)
<!--more-->

Apache Cordova is an open-source mobile development framework. 
It allows you to use standard web technologies - HTML5, CSS3, and JavaScript for cross-platform development
Apache Cordova enables software programmers to build applications for mobile devices using CSS3, HTML5, 
and JavaScript instead of relying on platform-specific APIs like those in Android, iOS, or Windows Phone.
![cordova](/resource/cordova/1.png)

cordova need node.js and npm development enviroment. 
## start
### Installing Cordova
```
$ npm install -g cordova.
```

### Create a project
```
$ cordova create MyApp cordova create MyApp
```

### Add a platform
* You can add ios, android, browser and so on.
```
$ cd MyApp

$ cordova platform add browser
```
### Run your app
* From the command line, run cordova run <platform name>.
```
$ cordova run browser
```

### Deploy the app
If you use mac, you can develop andorio and ios, But if you use other system, you can't develop ios.
* To deploy the app on a connected iOS device:
```
$ cordova run ios --device
```
* To deploy the app on a default iOS emulator:
```
$ cordova emulate ios
```
* You can use cordova run ios --list to see all available targets and cordova run ios --target=target_name to run application on a specific device or emulator (for example, cordova run ios --target="iPhone-6").
```
$ cordova run ios --list
$ cordova run ios --targets="iPad_Air"
```
You can also use cordova run --help to see additional build and run options.
