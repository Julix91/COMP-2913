---
layout: post
title:  "Component Lifecycle"
date:   2017-10-29 11:30:00 +0700
categories: [react]
---

#### What is it?

According to the official documentation: [React Component - Component Lifecycle](https://reactjs.org/docs/react-component.html#the-component-lifecycle)

> Each component has several “lifecycle methods” that you can override to run code at particular times in the process. Methods prefixed with "will" are called right before something happens, and methods prefixed with "did" are called right after something happens.

---

#### Available Lifecycle Methods

- [componentWillMount()](https://reactjs.org/docs/react-component.html#componentwillmount)

- [componentWillUnmount()](https://reactjs.org/docs/react-component.html#componentwillunmount)

- [componentDidMount()](https://reactjs.org/docs/react-component.html#componentdidmount)

- [componentWillReceiveProps()](https://reactjs.org/docs/react-component.html#componentwillreceiveprops)

- [componentWillUpdate()](https://reactjs.org/docs/react-component.html#componentwillupdate)

- [componentDidUpdate()](https://reactjs.org/docs/react-component.html#componentdidupdate)


- [componentDidCatch()](https://reactjs.org/docs/react-component.html#componentdidcatch)

Note that it is important to be aware of all of the lifecycle methods, but we will see limited use in class. Some of the methods above are used for more complex software/business requirements, and some are often used for improving an application's performance. Please read through the documentation above. I will also add my own comments on them below, from my experience using React over the past few years.

---

#### Instructor's Comments

Note that the comments below are based on the instructor's opinions and experiences, and may not be the only use cases for the lifecycle method above.

- componentWillMount() - This is one of the most useful lifecycle methods. Perfect place for making asynchronous requests for data from a remote server, or creating timeouts or intervals.

- componentWillUnmount() - This is the place to handle any cleanup that your component may require. This includes killing event listeners, timeouts and intervals, which can lead to memory leaks.

- componentDidMount() - This one is also very useful, specifically if you need access to the rendered components as soon as possible. Reasons for this include needing to attach an event listener to an element.

- componentWillReceiveProps() - Not as useful as the method above. In the past, I've used this for more complex logic that had to be run depending on the prop values received.

- componentWillUpdate() - Not very useful - mainly used for preparation when props and state change. But due to the fact that you cannot trigger a new state in this method, I've seen limited use for this.

- componentDidUpdate() - Also very limited use. It's a good place to manually access the DOM.

- componentDidCatch() - This is a new lifecycle method, and I haven't had the opportunity to use it yet, at the time of writing this. From the official documentation though, this sounds like a very useful method. Perfect for displaying a fallback UI or sending crash errors to a remote service.

---

#### Implementing Lifecycle Example

See the Official Documentation for a good example: [React Component Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)

---
