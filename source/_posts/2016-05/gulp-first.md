---
title: gulp first
date: 2016-05-11 12:32:17
tags:
---
very first gulp example
<!--more-->
### 1. check node and npm
At first you have install node and npm.
```
npm -v (check out npm version)
node -v (check out node version)
```

### 2. install build tool
Install gulp and gulp-uglify to your dependencies at package.json
use manager user to do this is better.
```
sudo npm install --save-dev gulp
sudo npm install --save-dev gulp-uglify
```

### 3. write code
Create a gulpfile.js at the root of your project:
```
* gulpfile.js

var gulp = require('gulp');
var uglify = require('gulp-uglify'); 

gulp.task('default', function() {
gulp.src('example.js')
    .pipe(uglify()) 
    .pipe(gulp.dest('dist'))
});
```

### 4. create a example.js file for test.
```
cp gulpfile.js example.js
```

### 5. Run gulp 
```
gulp (Beacuse method name set as default, so you can run gulp not with method name)
```
### 6. Result
You will found that a dist directory had been created, and under dist, these has a file named example.js, this is the Compressed file.Like this
```
var gulp=require("gulp"),uglify=require("gulp-uglify");gulp.task("uglify",function(){gulp.src("example.js").pipe(uglify()).pipe(gulp.dest("dist"))});
```

* This is a good result that usually seen at big website's online js file. :)
![oceanpad.github.io](/resource/gulp/1.png)
![oceanpad.github.io](/resource/gulp/2.png)
