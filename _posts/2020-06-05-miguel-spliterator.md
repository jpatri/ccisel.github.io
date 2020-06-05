---
layout: post
title: Spliterator is not only about parallelism
date: 2020-06-05
type: post
published: true
status: publish
categories: []
tags: []
author:
  login: fmcarvalho
  email: 
  display_name: Miguel Gamboa
  
---

Many are still mistaken about the purpose of `Spliterator`. 
It is not only about parallelism.
`Spliterator` is the core traversing mechanism of Java Streams,
regardless of being processed in parallel or sequentially.
Whenever you build a `Stream` from an `Iterator` you are wrapping
it around a `Spliterator` and incurring in useless indirections.
Remember the answer stated by Bryan Goetz (author of Java streams)
to the question of Miguel Gamboa about the choice between `Iterator`
or `Stream` regarding laziness in a domain model design, namely:
* “_`Spliterator` has fundamentally lower per-element access costs than _Iterator_, **even sequentially**._”
  1. ” _The Iterator protocol is fundamentally less efficient._”
  2. “_`Spliterator` further offers a "fast-path" iteration_”

[Iterator versus Stream](https://stackoverflow.com/a/31212695/1140754)
