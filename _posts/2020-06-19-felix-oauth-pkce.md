---
layout: post
title: OAuth 2.0 and PKCE
image: 2020-06-19-felix-oauth-pkce.png
date: 2020-06-19
type: post
published: true
status: publish
category: Security
tags: []
author:
  login: pmhfelix
  email: 
  display_name: Pedro Félix
  image: felix.jpg
  role: Software Developer
---

The current
[“OAuth 2.0 Security Best Current Practice”](https://tools.ietf.org/html/draft-ietf-oauth-security-topics-15)
draft version recommends the use of PKCE (Proof Key for Code Exchange by OAuth
Public Client) to protect the authorization code grant flow, for all types of
applications and not only for native applications.
See this [post](https://blog.pedrofelix.org/2016/02/15/oauth-2-0-and-pkce/)
from CCISEL engineer Pedro Félix, where he describes the goals and mechanics of
PKCE.
