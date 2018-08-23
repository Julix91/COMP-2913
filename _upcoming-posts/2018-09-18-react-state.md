---
layout: post
title:  "React State"
date:   2018-09-18 10:00:00 +0700
categories: [react]
---

#### What is state?

According to a dictionary entry, this is the definition of state:

> the particular condition that someone or something is in at a specific time.

In Software Development, the term has pretty much the same meaning.

Here are some examples of state:

- When a user is inputting text into a text field. Each time the user types into the text field, the application is at a different state.

- When a user clicks on a checkbox, and it toggles from unchecked/checked.

- When you first load an application, and you see a loading spinner. Then moments later, you see a list of data that was not there before.

- In a game, where you take damage from an enemy, and your health bar lowers.

- In a calculator, when you input your 1st number, 2nd number and operator.

If you think about it, software cannot exist without state. Otherwise they'd just be static content, that cannot be interacted with, such as books, movies and static websites.

---

#### How to use State in Components

In React, there are a few different ways that you can create Components. We've learned one of them, which will have you covered for all our cases. We will cover other ways of creating components at a future class.
If you are using JavaScript's `class` constructor to create components, here is how you can implement state:

{% highlight react %}
import React, { Component } from 'react';

class CurrentDate extends Component {
  constructor(props) {
    super(props);

    this.state = { date: new Date() };
  }

  render() {
    return (
      <div>
        <p>Hello {this.props.name}!</p>
        <p>Current Date: {this.state.date.toLocaleTimeString()}</p>
      </div>
    );
  }
}

export default CurrentDate;
{% endhighlight %}

If you render the component above, you will notice that the current date gets displayed every time you refresh your browser. So what is happening on the code above?
Before reading the explanation below, take a few minutes to study the snippe above, and see if you can make sense of it.

##### Explanation

A lot of things are happening on the component above. Here is a breakdown of what's happening:

1. First the CurrentDate Component is defined.

1. Note the constructor function inside of the CurrentDate class. In ECMAScript 6, we now have the ability to create `classes`, which is just syntax sugar for functions. I recommend reading on JavaScript classes at home. Essentially, if the constructor function exists, it will be called when a new instance of the class is created. This means that for every instance of the Component you render, the constructor will be called for each of those components.

1. If you create a React component without a constructor, it will use the `React.Component`'s constructor instead. Why? Because the Components we create extend from `React.Component`.

1. If we do add a constructor function, you will see that we call `super(props)`. This doesn't mean that props are awesome. What this does is it call it's parent's contructor (`React.Component`'s).

1. We then assign a value to `this.state`. Since we do this inside of the constructor, we call this the **Initial State**.  If you do decide to give state a value, it should always be an Object. The value that we gave to the CurrentDate initial state is `{ date: new Date() }`.

1. In the render function, we have access to the state above. we can access state similarly to how we access props. `this.state`.

You can use both state and props in the same Component. Often, state will be used a props for your Component's children components. We now know how to use state, but it still doesn't seem very useful, does it? How do we manipulate state to handle user interactivity? Before moving on, make sure you have a good understanding of the material up to now. Things are about to get really interesting!

Meanwhile, see the Official Docs on State here:
[React Docs - State & Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)

---
