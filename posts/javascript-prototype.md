---
title: 'Object-Oriented Programming in JavaScript (Part I)'
subtitle: 'Objects and Prototyping'
date: '2020-11-08'
---

<h2>Intro</h2>

Blogging is a staple in a developer's learning path. Unfortunately I've been on my path for a year and for some reason thought it was just as good to document my learning on paper. So for the next few days I will be back-logging all of my handwritten notes while referring to some written works that will be credited at the end of each part. It's going to be a long week but I'm feeling good and just had my morning coffee. 

<h2>Object Oriented Programming</h2>

One way of using JavaScript is to use a set of techniques that focuses organization around the use
of objects called <em>object-oriented programming</em>. This approach is older than JavaScript itself.
In fact, JavaScript's design as a language was shaped by object-oriented programming. Today I will
break down some of the ways it is applied in JavaScript.

At its core, object-oriented programming divides programs into smaller programs (modeled with objects), each with their own localized state and logic. This keeps each piece of your program independent of each other's changes in state or logic. These pieces communicate through interfaces, logic that abstracts their functionality. Interfaces consist of <em>public</em> methods and <em>properties</em>. Contrary to public properties, <em>private</em> properties do not interact with anything outside it's piece.

It should be noted that JavaScript does not distinguish between the former and the latter. However, it has become customary to use underscores (_) at the beginning of property names to indicate that the property is private. 

Methods are properties whose values are functions. Calling a method's property uses <em>this</em> to indicate a binding to its parent object.

<h2>Prototypes</h2>

Most JavaScript objects have built-in <em>prototypes</em>, objects used as a fallback source of properties. You can call the prototype of an object with <kdb>Object.getPrototypeOf</kdb>. The prototype of an empty object {} is <kdb>Object.prototype</kdb>--the ancestral prototype. Object prototype relations form a tree-structure, with <kdb>Object.prototype</kdb> at the root. It contains built-in methods that all objects have access to.

Objects themselves don't necessarily have <kdb>Object.prototype</kdb> as their prototype. Instead, their prototypes are other objects that provide differing defaults. Functions, being objects themselves, derive from<kdb>Function.prototype</kdb>. Similarly arrays, also objects, derive from <kdb>Array.prototype</kdb>. In other words, objects contain prototypes, which contain prototypes, and so on and so forth until you reach <kdb>Object.prototype</kdb>.

> *Methods To Remember*
> * <kdb>Object.toString</kdb> returns a string representation of the object.
> * <kdb>Object.create</kdb> creates an object with a specified prototype.

I haven't even scratched the surface of OOP. Stay tuned for part II where I will touch more on Javascript Classes!

---

<h2>Works Cited</h2>

> Haverbeke, Martin "The Secret Life of Objects" <em>Eloquent JavaScript > > - A Modern Introduction to Programming</em>, 3rd Edition, 2019, Chapter > 6, No Starch Press, Inc.