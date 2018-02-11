---
layout: post
title:  "Conditional Rendering"
date:   2018-03-12 13:00:00 +0700
categories: [react]
---

In your application, depending on the state, you may want to display/hide certain things.

Examples of when conditional rendering can be used:

- If a user is logged in, you may want to display a welcome message. Otherwise, you may want to display a Login button.

- If your current physical location is displayed on the map, you may want to display a pin icon.

- If there are results for your search, you may want to display a list. Otherwise, you may want to display a "no results found" message.

Please see [React - Conditional Rendering](https://reactjs.org/docs/conditional-rendering.html) for up to date examples.

---

#### Exercise:


- Create 2 components. 1 called "HomeView" and another called "LoginView".

- Have a different message on each of these components.

- At your top-level component (usually <App />), set the initial state for "isLoggedIn" to false.

- Render the HomeView if "isLoggedIn" is true. Render the LoginView otherwise.

- Set the initial state of "isLoggedIn" to false to test that your conditional works.

---
