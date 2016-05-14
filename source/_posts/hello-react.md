---
title: hello react
date: 2016-05-15 00:18:45
tags:
---
Leaning facebook react
<!--more-->
## xdg-open(not about react)
### open html file by default application directly by command line
```
xdg-open index.html
```
### config xdg-open
xdg-open is configured by the files mentioned in Default applications. 
xdg-mime modifies the local file ~/.config/mimeapps.list and 
~/.local/share/applications/mimeapps.list (deprecated).
```
vi ~/.config/mimeapps.list
```


## react
You can download react starter kit at react Doc. Under this kit folder, you can find two folders.
### build
This folder contains react framework files, such as react.js, react-dom.js, react.min.js and so on.
### examples
This folder contains many react start examples. You can practice your react skill by these exsmples.

### my react github address
```
git clone git@github.com:oceanpad/react.git
```
I will write some codes under training folder

### start react code
With react, you can write html code into javascript code, and it work well. That is so cool.
helloword.html
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Hello React!</title>
    <script src="../build/react.js"></script>
    <script src="../build/react-dom.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/5.8.23/browser.min.js"></script>
  </head>
  <body>
    <div id="example"></div>
    <script type="text/babel">
      ReactDOM.render(
        <h1>Hello, world!</h1>,
        document.getElementById('example')
      );
    </script>
  </body>
</html>
```
* The XML syntax inside of JavaScript is called [JSX](https://facebook.github.io/react/docs/jsx-in-depth.html).
* In order to translate it to vanilla JavaScript we heve to use <\script type="text/babel">.
* You don't have to use JSX with React. You can just use plain JS.

 [facebook react homepage](https://facebook.github.io/react/index.html)
