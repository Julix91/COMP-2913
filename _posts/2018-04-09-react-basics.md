---
layout: post
title:  "React Basics"
date:   2018-04-09 21:30:00 +0700
categories: [react]
---

#### Initial Project

If you have used [Create React App](https://github.com/facebookincubator/create-react-app) to scaffold your first React Application, you should be able to use `npm start` on your terminal to start your application server. Once the server is running locally, you should be able to see it on your browser by going to localhost:3000.

- Use your editor of choice to open your newly created project.
- See src/App.js.
- Find the h1 tag in App.js, and change it's text node, from "Welcome to React", with your name.
- Save the file and see your page on your browser.

Did the changes get reflected on the page?

The App.js file that you modified is a React Component. React components get rendered into your html document. Basically, the React rendering engine looks at your JavaScript, then translates them into html, which browsers can in turn, display properly.

How does React know where to render your application in the html?

Look at public/index.html. If you are familiar with Web Development, you will know that this is usually the entry point for a website. Look for the html line below:

{% highlight html %}
<div id="root"></div>
{% endhighlight %}

Now look at src/index.js. In this project, this file is the entry point for your JavaScript application.

{% highlight js %}
ReactDOM.render(<App />, document.getElementById('root'));
{% endhighlight %}

Are you starting to see the connection? The JavaScript is rendering your "App" component, into the html element with id "root". Very rarely you will need to modify this public/index.html and src/index.js files. Just keep in mind that there's no magic going on here. At it's most basic form, React is adding html code into your index.html file, by looking at your App component. That's it!

Also see [https://reactjs.org/docs/hello-world.html](https://reactjs.org/docs/hello-world.html) in the official React documentation.

---

#### What is JSX?
See [https://reactjs.org/docs/introducing-jsx.html](https://reactjs.org/docs/introducing-jsx.html)

---

#### Your first React component

All of your JavaScript code should live inside of the src/ directory. You may add sub-directories for organization purposes. This is recommended. Let's try creating a component called "Profile".

- First, create a new file called Profile.js, under src/components/.
- In your new blank file, type the following out (don't copy and paste. Typing it out will help you remember the React Component structure better.)

{% highlight react %}
import React, { Component } from 'react';

class Profile extends Component {
  render() {
    return (
      <div>
        <img src="some/image/url" />
        <span>My Name</span>
      </div>
    );
  }
}

export default Profile;
{% endhighlight %}

Will creating the component above render it on your html page? Go and take a look.

You will soon notice that just creating the component above will not affect your html page at all. Where would it get displayed?
Open your App.js file and let's display your new Component. We will do this together in class.
Essentially, you will need to render your new component inside of the App component!

---

#### Props

Now let's say we would like to display a Profile for your instructor. Would you need to create an entirely new component for that? That doesn't sound very scaleable! What if you were Facebook, and had to display a list of all your friends? You don't want to have a separate file for each person in the World. What you need is a template, into which you can specify variables, like name and image link.
This is where "props" come in. By specifying props, you can pass in different values into your Profile component. Example:

{% highlight react %}
import React, { Component } from 'react';

class Profile extends Component {
  render() {
    return (
      <div>
        <img src={this.props.imageUrl} />
        <span>{this.props.name}</span>
      </div>
    );
  }
}

export default Profile;
{% endhighlight %}

and to use your component with different props:

{% highlight react %}
<Profile name="Your Name" imageUrl="your image url" />
<Profile name="Daniel Takeuchi" imageUrl="some other url" />
{% endhighlight %}

See more at: [https://reactjs.org/docs/components-and-props.html](https://reactjs.org/docs/components-and-props.html)
