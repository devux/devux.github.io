---
layout: post
title:  "ReactJS with Webpack and Babel"
date:   2016-03-30 12:57:14 +0530
categories: Technical
author: devux@devakumar.mj
---

# Why ReactJS?
Before three months I don't even know what is front end framework then I started AngularJS for some 2 to 3 days I cant undertsnd angular formats and directory structor etc.After sometime I started React for some 2 to 3 days and again I cant understand the formats and directory structor etc after then I come to that the problem is not the framework which we are using.the problem is how we learning the framework ???<br/> 
Apart from that no more reason for me to use ReactJS may be the perfomance,implementaion,plugins and functionality are better then other framework but I'm not sure about that because I didn't used ReactJS yet.So I've trying ReactJS for a while in this blog I'll explain how setup ReactJS with webpack and babel.<br/>
Note: This blog is more suitable for Gnu/Linux based Operating System

# Install npm and node (Step 1)
To install You can follow the instruction here <br/>
[Installation Steps Here](https://github.com/npm/npm)<br/>
or <br/>
[Another Intallation Steps here](https://docs.npmjs.com/getting-started/installing-node)

# Create a project directory and set as npm project
1.Create a new directory using this command <br/>
`mkdir reactapp`<br/>
2.move inside to the directory <br/>
`cd reactapp`<br/>
3.make it as npm project<br/>
`npm init`

![Screenshot from my machine](/images/react1.png)

After entering this you should supposed to answer for some questions to make package.json file for your app.don't worry about that you can also skip the qeustions by pressing enter.At the end package.json file created inside your app with the details which you have given during previous answering step.Yes now this becomes a node project.

![Screenshot from my machine](/images/react2.png)


# Install react using npm
You can install react in this project by using the command<br/>
`npm install react

npm install react-dom`

If you want to save this configuraion in your package.json file you can use the command as<br/>
`npm install --save react`<br/>
`npm install --save react-dom`

If you want to install specfic version of react you can use the following command<br/>
`npm install --save react@0.14.7`

`npm install --save react-dom@0.14.7`

# why babel? and Installing Babel

we will be writing some script in react which is not in the format of javascript so babel is used to convert some form of script into javascript.<br/>
you can install babel in this project in the same way with some dependency
`npm install --save babel-loader@6.2.1`<br/>
`npm install --save babel-core@6.4.5`<br/>
`npm install --save babel-preset-es2015@6.3.13`<br/>
`npm install --save babel-preset-react@6.3.13`<br/>
After doing this you can open your package.json and see the difference that npm packages are listed inside dependency with this package.json file you can install all the packages using this command

`npm install`

# Creating html 
let create a new directory(folder)<br/>
`mkdir public`<br/>
`cd public`<br/>
lets create a html file called index.html<br/>
`touch index.html`<br/>
Have some simple html in that file<br/>
`/public/index.html`<br/>

```
<!doctype html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Hello React</title>
  </head>
  <body>
    <div id="hello"></div>
    <script src="bundle.js"></script>
  </body>
</html>
```


# First react Component

Dont worry Im don't want to bore you by explaining each step of react compenent I'm just pasting simple HelloWorl react component here

`mkdir app`<br/>
`cd app`<br/>
`mkdir component`<br/>
`cd component`<br/>
`touch Main.js`<br/>
your Main.js should look like this<br/>

```
import React from 'react';
import ReactDOM from 'react-dom';
 
class Hello extends React.Component {
  render() {
    return <h1>Hello Devux this is my first React App</h1>
  }
}
ReactDOM.render(<Hello/>, document.getElementById('hello'));
```


# Installing Webpack
By the same way you can install webpack<br/>
`npm install --save webpack`

# webpack.config.js

After installing webpack you just create a file called webpack.config.js which contails some configuration details <br/>
Entry point: entry point of reactjs component<br/>
Output: path to file where to save converted form of javascript<br/>
Module: dependency confugured<br/>
you webpack.config.js looks like this<br/>

```
module.exports = {
  entry: './app/component/Main.js',
  output: { path: __dirname, filename: 'public/bundle.js' },
  module: {
    loaders: [
      {
        test: /.jsx?$/,
        loader: 'babel-loader',
        exclude: /node_modules/,
        query: {
          presets: ['es2015', 'react']
        }
      }
    ]
  },
};
```

# Running Webpack

use this command for webpack compilation process

`webpack -w`

![Screenshot from my machine](/images/react3.png)


After this a bundle.js file will be created inside public deirectory as we mensioned in webpack.config.js


Now you can the index.html with browser

and see the result in browser like this

![Screenshot from my machine](/images/react4.png)

I will write more blog on react while I'm learning............

                                  ********


