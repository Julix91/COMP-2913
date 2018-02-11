---
layout: post
title:  "React Introduction"
date:   2018-02-10 18:30:00 +0700
categories: [react]
---

#### What is React

- It is a JavaScript library for building User Interfaces.
- It’s open source
- Started in 2013.
- Can currently be used to develop browser and native mobile applications
- Created by Jordan Walke, a Software Engineer at Facebook. It is currently maintained by Facebook, Instagram and other individual contributors.
- Allows developers to create complex single-page or server rendered applications.
- It’s fast, simple and scalable.

---

#### Who uses React?

<ul style="display: inline-flex; list-style: none; padding: 0;">
  <li><img src="/COMP-2913/static/img/company_logos/airbnb.png" alt="airbnb" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/coursera.png" alt="coursera" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/dropbox.png" alt="dropbox" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/facebook.png" alt="facebook" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/flipboard.png" alt="flipboard" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/instagram.jpg" alt="instagram" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/netflix.png" alt="netflix" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/pinterest.jpeg" alt="pinterest" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/twitter.png" alt="twitter" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/uber.png" alt="uber" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/wordpress.png" alt="wordpress" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
</ul>



- Airbnb
- Coursera
- Dropbox
- Facebook
- Flipboard
- Instagram
- Netflix
- Pinterest
- Twitter
- Uber
- Wordpress
- …and thousands more big and small companies

*Source: [React on Github](https://github.com/facebook/react/wiki/sites-using-react)*

---

#### Alternatives to React

Although React is not a full-fledged front-end JavaScript framework, it often is used as the base of full applications. Alternatives to React include:

<ul style="display: inline-flex; list-style: none; padding: 0;">
  <li><img src="/COMP-2913/static/img/company_logos/angular.png" alt="angular" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/vue.png" alt="vue" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/ember.png" alt="ember" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/meteor.png" alt="meteor" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
  <li><img src="/COMP-2913/static/img/company_logos/backbone.png" alt="backbone" style="width: 48px; margin-right: 10px; border-radius: 5px;" /></li>
</ul>


- Angular
- Vue.js
- Ember
- Meteor
- Backbone.js

---

### How does React compare with other frameworks?

- React is a light-weight library for building user interfaces, whereas other frameworks follow the MVC (Model View Controller) architecture. React would only be the “V” in MVC.
- Currently the fastest growing JavaScript “framework”.
- Generally easier to learn.
- More adaptive and flexible, as there’s less standards set by the framework itself. This means that more choice is available on what libraries to use to build the base of your application.

---

### The flexibility of React

- Can be used for single page applications or server rendered web pages.
- Usable in the browser or in native mobile applications.
- Option to use JSX or vanilla JavaScript.
- Option to use Babel, which gives developers the ability to use new ECMAScript 6 features. Alternatively, vanilla ES5 JavaScript.
- Wide variety of libraries compatible with React.
- Supports all major browsers and Internet Explorer 9 onwards.

---

### Before Getting Started

As React is still evolving, often new tools and features are added over time. In this class,
I'll link to the actual React documentation, so that we have access to the latest up-to-date information.
Please keep in mind that although the core concepts of the React library will likely not change drastically, often the API (Application Programming Interface) will. In order to ensure that these notes are always up to date, I'll link to the actual React documentation when applicable.
Also, as some initial setup is needed in order to run React on your computer, I strongly suggest that if you have a personal laptop, that you use it instead of BCIT's lab computers. This will save you the trouble of having to setup your machine every class.

---

### Getting Started

Please refer to this page:
[https://facebook.github.io/react/docs/installation.html](https://facebook.github.io/react/docs/installation.html)

There's a guide on how to create a new React app. We will do this together in class. Note that instructions may change, depending on your Operating System.

---

### Create React App

Currently, the easiest way to get started with React is with ["Create React App"](https://github.com/facebookincubator/create-react-app), a project maintained by Facebook. Create React App allows us to scaffold a new React project, with basic configuration and tooling all setup from the get-go.

```
// Directory structure (as of October 2017)

my-app

├── README.md

├── node_modules

├── package.json

├── .gitignore

├── public

│   └── favicon.ico

│   └── index.html

│   └── manifest.json

└── src

```

#### Project Structure

- **Readme.md** - This file is my-app's readme text file. The ".md" stands for markdown.

- **node_modules** - This directory contains the code for the package dependencies for your project. You will never need to edit the files in this directory manually.

- **package.json** - This file contains relevant project metadata and list of package dependencies and their accepted versions. These dependencies get installed into the node_modules directory. If you add a new dependency, the added package will be added to node_modules. If you remove a dependency, it will be removed from node_modules. Read more at [npm](https://www.npmjs.com/).

- **.gitignore** - List of files and directories to be ignored by [git](https://git-scm.com/). Git is a widely used version control system, used for small and large projects. [Github](https://github.com/), a software development platform, is built around git.

- **public** - Files that will be made available at the root of your client side React project. Mainly used for static assets, like images, and the base index.html file. You will rarely need to use this folder, as the index.html will be automatically updated for you as you work on your project.

- **src** - Contains all code related files in your project, including JavaScript and CSS files. The entry point for your JavaScript code is **src/index.js**, which is where my-app's React will kick in.

---
