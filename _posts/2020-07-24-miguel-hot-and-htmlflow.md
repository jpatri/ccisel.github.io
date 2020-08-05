---
layout: post
title: Unleash Web Views with Higher-order Templates - HtmlFlow
image: 2020-07-24-miguel-hot-and-htmlflow.png
date: 2020-07-24
type: post
published: true
status: publish
category: Template Engines and DSL
tags: [Java, async, CompletableFuture, Task, Promise, Kotlin]
author:
  login: miguelgamboa
  email: 
  display_name: Miguel Gamboa
  image: miguel.jpg
  role: Software Developer
---

Using server-side Web templating to render an HTML listing with 1000 records
resulting of 20 pages with 50 items each, from a Web API with a rate limit of 1
req/sec, then you will need 20 seconds to join all data and render the web page.
Front-end development avoids it through infinite scrolling and other similar techniques. 
In 
[“_HoT: Unleash Web Views with Higher-order Templates_”](https://www.scitepress.org/Link.aspx?doi=10.5220/0008167701180129),
the CCISEL Engineer Miguel Gamboa, takes advantage of a Java DSL for HTML –
[HtmlFlow](https://github.com/xmlet/htmlflow) – to achieve a progressive rendering without
blocking the template resolution on the server-side. This presentation includes
a demo ([http://topgenius.eu](http://topgenius.eu)) comparing 3 different approaches: Handlebars
(server-side), React (front-end) and HtmlFlow (Java DSL for HTML).

<a href="https://htmlflow.org">
  <img src="/assets/blog/2020-07-24-miguel-hot-and-htmlflow.png" width="720px">
</a>