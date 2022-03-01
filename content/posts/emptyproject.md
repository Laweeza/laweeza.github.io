---
title: "React Project Skeleton"
date: 2022-02-28T00:23:37-08:00
description: "Trying not to use npx-create-react-app"
draft: true
series:
  - react
tags: ["react"]
---


![An Empty File](/images/empty.png)

As tempting as it would be to use `npx-create-react-app` to spin up a boilerplate for my new project, I decided to force myself to build my project from scratch.

1) To create a `package.json` file, use `npm init -y`. A `package.json` should pop up in the file. Including `-y` in the `npm init` bypasses the questions that usually come with setup.

* Filled out the author portion and a couple of keywords for now. Moving on...

2) It's best to create a `LICENSE.txt` for an open-source project so that users are free to use, change and distribute the software. Without a license the default copyright laws apply. I'll opt out for now.


3) The next step would be to create a public folder which will hold all of the CSS, image assets, and HTML markup. The HTML will serve the React app and attach it to the div element with ID of root.

![HTML File](/images/html.png)

4) Install react and react-dom: `npm i react react-dom`.

5) Install babel: `npm install @babel/core @babel/preset-env @babel/preset-react babel-loader --save-dev.`

6) Install webpack: `npm install --save-dev webpack webpack-cli webpack-dev-server`. Even if `webpack-cli` (command line tool) is installed globally, it is not installed in the current project and will need to be re-installed.
