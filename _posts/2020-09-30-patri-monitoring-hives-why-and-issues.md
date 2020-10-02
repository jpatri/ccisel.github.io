---
layout: post
title: Monitoring hives? Why and issues.
image: 2020-09-30-patri-monitoring-hives-why-and-issues-front.jpg
date: 2020-10-02
type: post
published: true
status: publish
category: Embedded systems
tags: [TrackBees]
author:
  login: jpatri
  email: jpatri@cc.isel.ipl.pt
  display_name: João Pedro Patriarca
  image: patri.jpg
  role: Software Developer
---

What challenges faces an anti-theft system and GPS tracker for beehives? Power supply? Networking? What else? The CCISEL Engineer João Pedro Patriarca is the author and developer of the TrackBees project started in 2012, which answers those and other questions. Since then, the TrackBees has been enhanced in different releases with several innovations that will be explained in this series of posts. This is the first post describing the motivation and the main issues tackled by this project.

## Motivation

The main loss of stolen beehives is not only the hives and honey, but, mainly, the honey workers, the bees.
This led to the idea of creating a device that could detect, signalize and recover stolen hives.

## Issues

There are some issues to consider when designing a solution to this problem, mainly because the apiaries are installed remotely:

* Normally, there is no permanent power supply;
* The hives must not evidentiate the presence of an electronic device;
* The communications infrastructure are limited;
* Determine the position in open space.

Based on the above issues, we have defined the first device characteristics:

* Must be powered by battery;
* The battery charge should last for months; This specificity became the main focus in designing the solution;
* The device must be small enough to be installed inside the hive;
* Integrates a GSM module for communications;
* Integrates a GPS module to determine current position.

This was the release of 2014. The image shows the front and the rear of the same board. Wait for next posts to see further details and improvements!

<img src="/assets/blog/2020-09-30-patri-monitoring-hives-why-and-issues-front.jpg" width="720px">


**Next post**: battery charge should last for months.
