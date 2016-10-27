---
layout: post
title:  "Create and Deploy React in firebase"
date:   2014-06-26 12:57:14 +0530
categories: Technical
author: devux@devakumar.mj
---


  After installing [npm and node](https://docs.npmjs.com/getting-started/installing-node) you can easily create a react app and deploy in to any platform,Here I'm using firebase.

### Step 1:
Install [create-react-app](https://github.com/facebookincubator/create-react-app)

```
npm install -g create-react-app

create-react-app my-new-app

cd my-new-app

npm start

```

### Step 2:
Then open [http://localhost:3000](http://localhost:3000) to see your app.

### Step 3:
Create free accout in [firebase](https://firebase.google.com) and create a repository.

### Step 4:
Login into firebase

```
npm install -g firebase-tools

firebase login

```
It will redirect to a link in browser,After clicking the link you are logged into firebase.

### Step 5:
Inside your app directory

```
firebase init

```
It will ask to choose some option like selecting firebase repo to host. After finishing this configuration you can find ``` firebase.json ``` in your app.

### Step 6:

one more command is more to deploy your app in to firebase  

```
firebase deploy
```

finally your got hosted in firebase like [my-new-app.firebase.com](my-new-app.firebase.com)

Happy Coding ;) 