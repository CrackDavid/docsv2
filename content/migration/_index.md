+++
title = "Migration Guide"
date = 2020-12-29T19:33:11+10:00
weight = 1
+++

Here are the steps to migrate your current v1 project to v2:

0. update your local wails environment to 2.0.0 using ``wails update``
1. Create a ``wails.json`` file in the root of your project containing the following:

  ### Vue.js
  ```
  {
    "name": "YOURPROJECTNAME",  
    "outputfilename": "YOURBINARYNAME",
    "html": "frontend/dist/index.html",
    "js": "frontend/dist/app.js",
    "css": "frontend/dist/app.css",
    "frontend:build": "npm run build",
    "frontend:install": "npm install"
}
  ```
  ### Svelte

 ```
  {
    "name": "YOURPROJECTNAME",  
    "outputfilename": "YOURBINARYNAME",
    "html": "frontend/public/index.html",
    "js": "frontend/public/bundle.js",
    "css": "frontend/public/bundle.css",
    "frontend:build": "npm run build",
    "frontend:install": "npm install"
}
  ``` 

  2. change all of your go import statements from ``"github.com/wailsapp/wails"`` to ``github.com/wailsapp/wails/v2``
  3. change your main create app call ``wails.CreateApp`` to ``wails.CreateAppWithOptions``
  4. remove the ``Wails.Init`` function in your main frontend file and just leave the functions inside of it.


Also we should add some sections about changed functions:

- Dialog changes 
- arbitrary functions in wails.bind