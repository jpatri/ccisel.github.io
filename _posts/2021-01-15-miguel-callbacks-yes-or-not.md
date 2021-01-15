---
layout: post
title: Can we teach Node Js without callbacks?
image: 2021-01-15-miguel-callbacks-yes-or-not.png
date: 2021-01-15
type: post
published: true
status: publish
category: web
tags: [web]
author:
  login: miguelgamboa
  email: 
  display_name: Miguel Gamboa
  image: miguel.jpg
  role: Software Developer
---

After another semester teaching Web Development the following question arises to
my mind: _can we teach Node Js without callbacks_?
Considering that we cannot avoid Promises and async/await, so should we
continually introduce callbacks in the first place? Notice that:
1. Most part of Node API already supports Promises, e.g. file system module `fs`
2. Starting lecturing with a simple use case of an HTTP client it is
   increasingly difficult to find a Node module that provides callback-based
   API. One of those most used modules, i.e. `request` (with 23M downloads/week)
   announced that is fully deprecated in February of 2020.

Of course, we can always use the standard `http` module of Node, yet its API is
far from being quite friendly. 

Thus, this leads me to think that we could remove callbacks from the curricular
plan of Web Development course. Can we?

Yet, some of the state-of-the-art frameworks for web development in the
Javascript ecosystem are still based on callbacks, namely: 1) express, 2)
passport. Of course there are a couple of wrapper alternatives that provide a
promise-based abstraction layer over these modules. But none of those approaches
was adopted as a best practice over the plain use of express or passport.

So, now regarding these latter points I will tend to consider that we should
also keep callbacks-based calling convention in the curricular plan of Web
Development course. Or not?