---
layout: post
title:  "Asynchronous requests"
date:   2018-04-30 12:00:00 +0700
---

#### Making Asynchronous HTTP requests in React

The React library does not include any utilities for making HTTP requests. Since React only renders Views, we have the flexibility to chose how we handle our application's requests.

---

#### Options

There are dozens of libraries to chose from, to facilitate your HTTP requests. It's even possible to do it with the vanilla JavaScript API, although it's not recommended. This is because most of the time, a high-level library will take care of most of the complexity in making these requests.

Here are a few libraries/APIs that handle HTTP requests:

- [Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) - a relatively new vanilla JavaScript API, which is a lot simpler to use then the old XMLHttpRequest API.

- [axios](https://github.com/axios/axios) - Promise based HTTP client. Highly recommended.

- [SuperAgent](https://visionmedia.github.io/superagent/) - Lightweight library for handling requests.

- [jQuery](https://jquery.com/) - A full-blown JavaScript library, with tons of utilities. Since a lot of the jQuery does not play well with React, this one is not recommended for this course.

- [XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) - The old JavaScript API for making AJAX requests. All libraries above are built on top of this API. Not recommended, unless you need a very customized http request handler.

---

#### Exercise

Use a public API to request a list of all countries, and display them in a React App.

1. Create a new application called countries-list.

1. Install your HTTP Request library of choice. I recommend [axios](https://github.com/axios/axios).

1. To fetch a list of countries in JSON format, make the following request:

    **GET** *https://restcountries.eu/rest/v2/all*

1. Display a loading spinner while the request is being made.

1. Display the list of countries.

1. Each country you list must also display their capital city and continent.

1. Using the [REST Countries API](https://restcountries.eu/#api-endpoints-all) as reference, add the ability to search for countries in your app. You can use a text input and a button to fire the search.
