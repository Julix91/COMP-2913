---
layout: post
title:  "Component Lifecycle"
date:   2018-09-18 11:30:00 +0700
categories: [react]
---

#### What is it?

According to the official documentation: [React Component - Component Lifecycle](https://reactjs.org/docs/react-component.html#the-component-lifecycle)

> Each component has several “lifecycle methods” that you can override to run code at particular times in the process. Methods prefixed with "will" are called right before something happens, and methods prefixed with "did" are called right after something happens.

---

#### Available Lifecycle Methods

- DEPRECATED - [componentWillMount()](https://reactjs.org/docs/react-component.html#componentwillmount)

- [componentWillUnmount()](https://reactjs.org/docs/react-component.html#componentwillunmount)

- [componentDidMount()](https://reactjs.org/docs/react-component.html#componentdidmount)

- DEPRECATED - [componentWillReceiveProps()](https://reactjs.org/docs/react-component.html#componentwillreceiveprops)

- DEPRECATED - [componentWillUpdate()](https://reactjs.org/docs/react-component.html#componentwillupdate)

- [componentDidUpdate()](https://reactjs.org/docs/react-component.html#componentdidupdate)

- [componentDidCatch()](https://reactjs.org/docs/react-component.html#componentdidcatch)

- [shouldComponentUpdate()](https://reactjs.org/docs/react-component.html#shouldcomponentupdate)

- NEW - [getDerivedStateFromProps()](https://reactjs.org/blog/2018/03/27/update-on-async-rendering.html#new-lifecycle-getderivedstatefromprops)

- NEW - [getSnapshotBeforeUpdate()](https://reactjs.org/blog/2018/03/27/update-on-async-rendering.html#new-lifecycle-getsnapshotbeforeupdate)

Note that it is important to be aware of all of the lifecycle methods, but we will see limited use in class. Some of the methods above are used for more complex software/business requirements, and some are often used for improving an application's performance. Please read through the documentation above. I will also add my own comments on them below, from my experience using React over the past few years.

---

#### Instructor's Comments

Note that the comments below are based on the instructor's opinions and experiences, and may not be the only use cases for the lifecycle method above.

- componentWillUnmount() - This is the place to handle any cleanup that your component may require. This includes killing event listeners, timeouts and intervals, which can lead to memory leaks.

- componentDidMount() - This one is also very useful, specifically if you need access to the rendered components as soon as possible. Reasons for this include needing to attach an event listener to an element.

- componentWillReceiveProps() - Not as often used as the methods above. In the past, I've used this for more complex logic that had to be run depending on the prop values received.

- componentWillUpdate() - Not as often used as the method above. Mainly used for preparation when props and state change. But due to the fact that you cannot trigger a new state in this method, I've seen limited use for this.

- componentDidUpdate() - Also very limited use. It's a good place to manually access the DOM.

- componentDidCatch() - This is a new lifecycle method. Perfect for displaying a fallback UI or sending crash errors to a remote service.

- shouldComponentUpdate() - Mostly used for manual performance improvements, although it should be avoided when possible. Usage of this could potentially mean that you are trying to patch a badly architectured application.

- getDerivedStateFromProps() - This new lifecycle method is invoked after a component is instantiated as well as when it receives new props. It should be able to cover use cases for the deprecated `componentWillReceiveProps()` function.

- getSnapshotBeforeUpdate() - This new lifecycle method is called right before mutations are made (before DOM is updated). This method is often unneeded, but should be able to cover use cases for the deprecated `componentWillUpdate()`.

---

#### Implementing Lifecycle Example

See the Official Documentation for a good example: [React Component Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)

---
