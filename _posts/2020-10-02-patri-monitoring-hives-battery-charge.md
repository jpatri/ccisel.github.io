---
layout: post
title: Battery charge should last for months
date: 2020-10-10
type: post
published: false
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

Battery charge is an important issue in the hive monitoring device because we do not want to regularly go to the apiary just to charge the battery. So, how long should last the charge of a battery? Well, forever is the answer you want! Some may argue why do not to use a solar panel. Do not forget the device must be dissimulated inside the hive. This is the theme of this second post of TrackBees project. This post presents the solution used in TrackBees project so that a battery charge may last for months.

## Motivation

Two modules in the device are high power consuming: the GSM and GPS modules. These modules are only used in two scenarios:

1. In a theft scenario.
2. In a monitoring scenario.

Monitoring has been present in the solution since the beginning of the project, as it is necessary to ensure that the hive remains in the same installation position, that the SIM card has a balance to send SMS messages and that the battery has enough charge to keep the device working. In addition to these aspects, a temperature sensor was added to the solution to determine the hive's internal temperature. Even more, because the solution is not closed, other sensors may be integrated in the future like, for instance, weight sensor that enables the knowledge of honey evolution production.

## Solution

Since some modules in the solution are only used in sporadic scenarios, they may be constantly powered off and powered on only when needed. The expected monitoring cycles justify a complete disruption of power supply instead of using low power modes, normally supported in these modules.
The design of global system is base in two subsystems: subsystem one, with low power consuming that remains powered and is responsible to establish the power supply of subsystem two when an event occurs; subsystem two, that includes a microcontroller that is responsible for the execution of the control logic to identify a theft or to realize a monitoring cycle. The figure below illustrates a generic view of the system.

![TrackBees as two subsystems and one power supply control](/assets/blog/2020-10-10-patri-monitoring-hives-battery-charge.png)

<!--<img src="/assets/blog/2020-10-10-patri-monitoring-hives-battery-charge.png" width="720px">-->

The main components in subsystem one are an accelerometer to detect movement and a real time clock (RTC) to implement a calendar. Both produce trigger signals whenever a shit occurs or a date and time is reached. These signals are used to control the power supply of subsystem two.
In the figure we may see a third signal originated from microcontroller that is also used to control the power supply of subsystem two. This signal prevents disruption of power supply when trigger signals from accelerometer or RTC are disabled.

Next post: detailed description of the components in the 2014 release.
