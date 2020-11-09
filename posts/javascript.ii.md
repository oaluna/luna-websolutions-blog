---
title: 'Object Oriented Programming in JavaScript (Part II)'
subtitle: 'JavaScript Classes'
date: '2020-11-09'
---

<h2>Classes</h2>

Last time I was just beginning to cover object prototypes. If you haven't read part I of this series about object prototyping you can catch up on Part I of OOP [here](https://next-js-blog-piy6sy7x1.vercel.app/posts/javascript-prototype "Object Oriented Programming in JavaScript (Part I)").

Classes are a widely used take on prototypes. Classes define methods and properties for a type of object known as an <em>instance</em> of a class. Classes contain <em>constructor</em> functions, which ensures your instances share the parent class's properties. ReactJS classes explicitly call constructors for defining properties such as <kdb>this.state</kdb> and <kdb>this.handleChange</kdb>.

Outside of React, you can use <kdb>new</kdb> in front of your function to make it into a constructor function. It returns an object bound to your function with <kdb>this</kdb>. Your constructor function contains a <kdb>prototype</kdb> property, which can be called.

Since 2015 we have a simpler notation for classes:

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%2820%2C20%2C57%2C1%29&t=synthwave-84&wt=none&l=javascript&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=14px&lh=133%25&si=false&es=2x&wm=false&code=class%2520Hamburger%2520%257B%250A%2520%2520constructor%28type%29%2520%257B%250A%2520%2520%2520%2520this.type%2520%253D%2520type%253B%250A%2520%2520%257D%250A%2520%2520order%28build%29%2520%257B%250A%2520%2520%2520%2520console.log%28%27Give%2520me%2520a%2520%2524%257Bthis.type%257D%252C%2520%2524%257Bbuild%257D%2560%29%250A%2520%2520%257D%250A%257D%250Alet%2520doubleMeat%2520%253D%2520new%2520Hamburger%28%27Double%2520Meat%27%29%253B%250Alet%2520fourByFour%2520%253D%2520new%2520Hamburger%28%27Four%2520by%2520Four%27%29%253B%250A%2520%2520"
  style="margin: 15px 0 0 0; width: 100%; height:450px; border:0; transform: scale(1); overflow:hidden; scroll-behavior: none;">
</iframe>

As you can see, our constructor function is present along with methods declared. In this class notation the constructor and any methods are now packed together within the class's brackets. The methods declared within the constructor function, however, are bound to this particular instance using <kdb>this</kdb>. Other methods defined in a class are bound by default to the class's prototype. 

This is where you need to be careful when adding properties to your class declarations. If the property already exists in the object prototype, the existing property will be replaced, or overwritten. Contrary to its risks there is also use in being able to override properties, such as creating exceptional property values for specific instances of a class while allowing other instances of a class to continue deriving from their prototype.

Well that's it for Part II of Object Oriented Programming! I'll be posting rather frequently so stay tuned for Part III where I will tackle Maps!


---


<h2>Works Cited</h2>

> Haverbeke, Martin "The Secret Life of Objects" <em>Eloquent JavaScript > > - A Modern Introduction to Programming</em>, 3rd Edition, 2019, Chapter > 6, No Starch Press, Inc.