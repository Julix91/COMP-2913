---
layout: post
title:  "Installing npm packages"
date:   2018-03-19 10:00:00 +0700
---

#### What is npm?

[npm](https://www.npmjs.com/) is a package manager for JavaScript, allowing you to use libraries created by others in your own projects, or share them with others. React is an example of a library that can be managed through npm. Most modern projects use npm to manage their dependencies.

---

#### How can I see my project's dependencies?

Usually, your project dependencies are listed in **package.json**, at the root of your project. When running the command *npm install*, npm looks into this file to install all of your dependencies and sub-dependencies. All of these dependencies are installed into the node_modules directory by default.

---

#### How to install/remove libraries from my project?

{% highlight bash %}
# installs the moment package and adds it to package.json
npm install moment --save
# removes moment from project and package.json
npm uninstall moment
{% endhighlight %}

---
