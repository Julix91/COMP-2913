---
layout: post
title:  "React Router"
date:   2018-04-30 12:00:00 +0700
---

#### What is React Router?

[React Router](https://reacttraining.com/react-router/) is a popular library used by React Applications. It's actively maintained and is undergoing major changes over the years. Last year, a full revamp was released with version 4.
It bundles a set of Components used for navigation. As you know, React is used for creating single page applications. With the help of React Router, you can have the benefits of multiple views under different urls, nested routes, etc.

---

#### Adding the React Router to your application

```bash
npm install react-router-dom --save
```

---

#### Usage Examples

See an up to date example in the official documentation. We will try a simple implementation during class. [https://reacttraining.com/react-router/web/guides/quick-start](https://reacttraining.com/react-router/web/guides/quick-start)

---

#### Exercises

- Create a new React application

- Create a Navbar Component. This component will have links to different sections of your application.

- Under the Navbar Component, create links to: "Rock Paper Scissors Game" and "Countries List".

- Create components for each of those Views.

- Move code from past projects into this new project.

- Clicking on each Link should allow the user to see the respective project. These sub-projects should still work. If you have done it right, it should be very easy to reuse your old projects!

- Each of these views should have a unique url path. Use: `/countries` and `/rock-paper-scissors`.

- Add a redirect route for the countries list. If `/countries-list` is used as the url,
it should redirect to `countries`.

- Add a Not Found page, which will display if any route not matching your existing Views is accessed.

- Modify your Countries List code so that when you search for a country, it will add
that view to the browser history. Eg. `/countries/canada`. This should also work if the user first lands on your app through these paths.

---
