---
layout: post
title:  "JavaScript Object Immutability"
date:   2018-05-15 14:00:00 +0700
categories: [javascrit]
---

#### What is Immutability?

In programming, immutability means that a given data is "unchangeable" and cannot have it's state modified after being created.
In JavaScript, all primitive data types are immutable.

Example:

{% highlight js %}
let a = 'test';
let b = a;
a = a.toUpperCase();

console.log(a) // test
console.log(b) // TEST
console.log(a === b) // false
{% endhighlight %}

JavaScript Objects are mutable though. Meaning that they can change value once they are allocated space in memory.

{% highlight js %}
let carA = { model: 'Civic' };
let carB = carA;

a.model = 'Corolla';

console.log(carB.model); // Corolla
console.log(carA === carB) // true
{% endhighlight %}

Arrays in JavaScript are actually Object types as well, thus mutable.

{% highlight js %}
let a = ['apple', 'banana'];
let b = a;

a.push('cherry');

console.log(b); // ['apple', 'banana', 'cherry'];
console.log(a === b) // true
{% endhighlight %}

---

#### How does this affect us, developers?

Consider the code below.

{% highlight js %}
let age = 21;
let person = { name: 'John' };

someFunction(age);
someFunction(person);

console.log(age);
console.log(person);
{% endhighlight %}

What will be outputted to the console on the code above?
the number 21 will always be outputted.
As for person, this value could very well be mutated inside of "someFunction", and we cannot
determine the value just from the code above.

As you can imagine, this could cause a lot of confusion for programmers. Some architectural patterns even frown upon mutable objects, Redux being one of them.

---

#### Examples of functions that mutate Objects:

- Array.prototype.push
- Array.prototype.reverse
- Array.prototype.shift
- Array.prototype.sort
- Array.prototype.splice
- someObject[someProp] = newValue


#### Examples of functions that don't mutate Objects:

- Array.prototype.concat
- Array.prototype.filter
- Array.prototype.slice
- Array.prototype.map
- Object.assign({}, { [someProp]: someValue })
