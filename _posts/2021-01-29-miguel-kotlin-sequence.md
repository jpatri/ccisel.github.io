---
layout: post
title: Enhanced Streams Processing with Kotlin’s Sequence Interface?
image: 2021-01-29-miguel-kotlin-sequence.jpg
date: 2021-01-15
type: post
published: true
status: publish
category: java
tags: [java, kotlin]
author:
  login: miguelgamboa
  email: 
  display_name: Miguel Gamboa
  image: miguel.jpg
  role: Software Developer
---

Using Java libraries in the Kotlin ecosystem is a well-known approach. Yet, does
it also apply in the opposite direction? I.e. Does it make sense to use a Kotlin
library in Java? Yes, it can do. In the next [article](https://www.infoq.com/articles/enhanced-stream-kotlin-sequence/),
Diogo Poeira and Miguel Gamboa show you why? Particularly, to suppress the
overheads and lack of operation in Java streams API.

Despite the ingenious conception behind the Java streams package, it is not
obvious how to efficiently extend its API with user-defined operations. Moreover
its API lacks many useful operations such as _distinctBy_, _zip_, _collapse_, and many
others. To suppress those limitations several state-of-the-art alternatives have
been adopted such as Eclipse Collections, jOOλ, StreamEx or Vavr, but all of
them have limitations either on performance or in extensibility or even both. 

In their article titled “[_Enhanced Streams Processing with Kotlin’s Sequence Interface_](https://www.infoq.com/articles/enhanced-stream-kotlin-sequence/)”
Diogo and Miguel analyze the behavior of those libraries in a couple
of benchmarks in realistic use-cases and how Kotlin’s Sequence outperforms the
competition in a Java program.
