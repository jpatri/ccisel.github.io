---
layout: post
title: Battery charge should last for months (Monitoring hives - part 2)
image: 2020-10-10-patri-monitoring-hives-battery-charge.png
date: 2020-10-16
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

Battery charge is an important issue in the hive monitoring device to avoid the need of in-loco support just to charge the battery. So, how long should last the charge of a battery? Well, forever is the desired answer! Some may argue why not to use a solar panel. But, do not forget the device must be dissimulated inside the hive. This is the motivation for this second post about theTrackBees project. This post presents the solution used in the TrackBees project such that a battery charge may last for months.

## Motivation

There are two specific modules in the TrackBees device that are high power consuming: the GSM and GPS modules. These modules are only used in two scenarios:

1. In a theft scenario.
2. In a monitoring scenario.

Monitoring has been a primary requirement since the beginning of the project, as it is necessary to ensure that the hive remains in the same installation position, the SIM card has balance to send SMS messages and the battery has enough charge to keep the device working. In addition to these aspects, a temperature sensor was added to determine the hive's internal temperature. Even more, because the solution is not closed, other sensors may be integrated in the future like, for instance, a weight sensor that enables the knowledge about honey evolution production.

## Solution

Since some modules in the TrackBees device are only used in sporadic scenarios, they may be constantly powered off and powered on only when needed. The expected monitoring cycles justify a complete disruption of power supply instead of using low power modes, usually supported by these modules. This is one of the key ideas of the TrackBees project that answers a core requirement regarding the battery life cycle.  
The design of the global system is based in two subsystems: a) subsystem one, with low power consuming that remains powered and is responsible to establish the power supply of subsystem two when an event occurs; b) subsystem two, that includes a microcontroller that is responsible for the execution of the control logic to identify a theft or to perform a monitoring cycle. The following figure illustrates a generic view of the system.

![TrackBees as two subsystems and one power supply control](/assets/blog/2020-10-10-patri-monitoring-hives-battery-charge.png)

The main components in subsystem one are an accelerometer to detect movement and a real time clock (RTC) to implement a calendar. Both produce trigger signals whenever a theft occurs or a date and time is reached. These signals are used to control the power supply of subsystem two.
In the figure we may see a third signal originated from microcontroller that is also used to manage the power supply of subsystem two. This signal prevents disruption of power supply when signals triggered from the accelerometer or RTC are disabled.

**Next post**: detailed description of the components in the 2014 release.