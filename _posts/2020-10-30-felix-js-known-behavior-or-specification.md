---
layout: post
title: JavaScript known behavior or specification?
image: 2020-10-30-felix-js-known-behavior-or-specification.png
date: 2020-10-30
type: post
published: true
status: publish
category: Javascript
tags: [concurrent programing]
author:
  login: pmhfelix
  email: 
  display_name: Pedro Félix
  image: felix.jpg
  role: Software Developer
  
---

What is the expected behavior from the following usage that manages two Promises
(one rejected on creation and other fulfilled after a 100 milliseconds timeout),
which results in another rejected Promise?

```js
const f = async () => {
    const rej = Promise.reject(new Error("rej"));      // Rejected on creation
    const ful = new Promise(r => setTimeout(r, 1000)); // Fullfiled after 1000 ms
    await ful;                                         // Await for ful completion
    console.log('after await');                        
    await rej;                                           // Await for rej completion
}
f().catch((err) => {                        // On resulting Promise rejection then...
    console.log(`caught: ${err}`);
});
```