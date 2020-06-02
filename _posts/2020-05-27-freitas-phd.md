---
layout: post
title: Consistency properties in internet services
date: 2020-05-27
type: post
published: true
status: publish
categories: []
tags: []
author:
  login: ffreitas
  email: 
  display_name: Filipe Freitas
  
---

The CCISEL engineer and professor Filipe Freitas recently achieved his PhD in
the distributed systems area, namely on the study of consistency provided by
online services. Such problems are particularly important regarding the
expectations of software developers and users about the behavior delivered by
Web platforms, such as google, Amazon, Twitter and many others. Put it simply,
what is the acceptable result when you make a comment on some other’s post?
Should you see that comment on your next read? Most probably argue favorably. 

However, that kind of prospect is not free of costs and incurs in additional
overheads related with ensuring consistency properties. In his work Filipe
Freitas started to conduct a measurement study about the consistency properties
conveyed by several Internet services, which presented consistency anomalies,
including counter-intuitive behaviors, such as the lack of session write
monotonicity.  In the next step he demonstrated that it is possible to build a
middleware layer mediating the access to services offering fine-grained control
over the consistency semantics exposed to applications, by enriching the
properties originally offered by these services.