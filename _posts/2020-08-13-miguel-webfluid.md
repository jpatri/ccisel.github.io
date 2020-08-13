---
layout: post
title: WebFluid - reactive web streams
image: 2020-08-13-miguel-webfluid.png
date: 2020-08-13
type: post
published: true
status: publish
category: Reactive Streams
tags: [Stackoverflow]
author:
  login: miguelgamboa
  email: 
  display_name: Miguel Gamboa
  image: miguel.jpg
  role: Software Developer
---

The WebFluid project, lead by the CCISEL engineer Miguel Gamboa, has been
selected in 5th edition of R&D projects of Polytechnical Institute of Lisbon.
In this scope we will be extending the [HtmlFlow]( https://htmlflow.org/)
templating features to transparently deal with reactive models. 
Also, we will be exploring alternatives to reactive streams pipelines in
non-blocking IO scenarios ([javasync/RxIo]( https://github.com/javasync/RxIo)).
And finally composing these building blocks to form the WebFluid flow.

This project will also award a **research fellowship to an MsC student** to
join the WebFluid team. Soon we expect to announce the call for the
research fellowship. **Be alert!**

<img src="/assets/blog/2020-08-13-miguel-webfluid.png" width="500px" alt="WebFluid">

Simply put, the WebFluid project aims to optimize data flows on the Web between
services and applications through the elision of blocking IO operations. The
main goal is to ensure a reactive flow (non-blocking) from: 1) a data source, 2)
traversing several Web services transformations, 3) to the production of an end
user-interface in HTML.