---
layout: post
title: Monitoring hives, why and issues
date: 2020-09-30
type: post
published: false
status: publish
category: Embedded systems
<!---tags: [WebFluid]--->
author:
  login: jpatri
  email: jpatri@cc.isel.ipl.pt
  display_name: João Pedro Patriarca
  image: patri.jpg
  role: Software Developer
---

This is the first post of TrackBees project. This is a personal project and started in 2012. This post explain the motivation to do this work and the issues present in the solution.

## Motivation

It started with a honey production project, where several beehives were stolen from apiaries several times. The main loss was not only hives and honey, but, mainly, the honey producers, the bees.  
This took to an idea of to create a device that could detect, sinalize and recover stolen hives.

## Issues

There are some issues to take into account when designing a solution to this problem, mainly because the apiaries are installed remotely:

* Normally, there is no permanent power supply;
* Dissimulation of the presence of an electronic device;
* The communications infrastructure are limited;
* Determine the position in open space.

Based on the above issues, it was defined the first device characteristics:

* Must be powered by battery;
* The battery charge should last for months; This specificity became the main focus in designing the solution;
* The device must be small enough to be installed inside the hive;
* Integrates a GSM module for communications;
* Integrates a GPS module to determine current position.

Next post: battery charge should last for months
