---
layout: post
title: Test in real environment
image: 2020-12-03-patri-monitoring-hives-post4-test-with-bees-colony-frame-w-device.png
date: 2020-12-20
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

The status reached in the TrackBees equipment allowed us to perform a test in a real operating environment. During 2015, the equipment was installed in a hive in full activity, that is, in a hive with a bee colony. This post presents the experience, conclusions and the consequences of performing this test. In fact, "the consequences" was the most relevant aspect that was obtained with this test.

## Motivation

The TrackBees equipment in version v0.2 was subjected to [several tests](https://cc.isel.pt/embedded%20systems/2020/11/29/patri-monitoring-hives-tests-on-version-2014/) with the goal of assessing the operability of the equipment. However, all these tests were performed in a managed environment, that is, they were either performed in the laboratory or outside but in an empty hive. Therefore, there were a number of unanswered questions, such as: would installation in a hive compromise bees activity? Would communications in a rural environment be compromised? Would the reading of the geographical position be affected by the fact that the equipment is installed inside the hive? It became mandatory to test the operability of the equipment in a real environment. And so it happened... on a weekend, visiting an apiary, the equipment was placed inside a hive with bees.

## Preparation

A [traditional hive](https://en.wikipedia.org/wiki/Langstroth_hive) consists of one, two, or three boxes depending on the size of the bee colony and on the honey production. The boxes are stacked vertically, and inside each box is installed a set of eight to ten frames. Typically, in the lowest box lies the queen and the brood and, in the boxes above, is where honey is produced and stored.

For the test, a frame was prepared to contain the equipment. The preparation consisted of removing the wire from the frame used to fix the beeswax, closing the frame with two panels to avoid direct contact of the bees with the equipment and fixing the equipment on one of the panels. The figure below illustrates the frame prepared with the equipment fixed.

![Frame with Trackbees device](/assets/blog/2020-12-03-patri-monitoring-hives-post4-test-with-bees-colony-frame-w-device.png "Frame with Trackbees device")

## Experience

The experience of putting the equipment into operation in a beehive with bees revealed dramatic. The working environment was adverse considering the number of bees around, the proper clothing that did not help handling the equipment, the need for rapid intervention to reduce the disturbance of hive activity and, mainly, the setup of putting the equipment into operation. For example, in the version used in the test, the geographic position used as reference is collected by the equipment the first time it is connected to the battery. Once collected, the device sends it by SMS to the paired phone before transitioning to surveillance mode. The time involved to obtain the geographical position for the first time is usually long and can reach to, by experiences, 30 minutes because it is a "cold" reading, that is, first, it needs to acquire signal with any satellite and receive the entire satellites [almanac](https://www.e-education.psu.edu/geog862/node/1739) and, second, receive from four different satellites, at minimum, their [ephemeris](https://www.e-education.psu.edu/geog862/node/1737). So, all time corresponding to equipment initialization took place without realizing whether the equipment was operating properly, or not. By comparison, in the laboratory the equipment is connected to a terminal and directly observed the log messages produced by the equipment. In this reality, the same method to follow the initiation process was not possible because the equipment was closed inside a frame and installed inside a hive. However, it was done!

## Conclusions and consequences

After a few weeks in operation, it was observed that the bees maintained their normal activity, not accusing the presence of the equipment. When the frame with the equipment was removed from the hive it was verified only that the bees had sealed small holes and grooves of the frame with propolis not having interfered with the operation of the equipment. The equipment carried out the planned monitoring cycles by sending the collected data by SMS.

But the main aspect retained with this experience were the difficulties observed in the initial configuration of the equipment at the time of installation. This motivated the introduction of technology in the equipment to suppress the difficulties previously evidenced. This technological evolution had effects in both hardware and system control program.

A Bluetooth module for short-distance wireless communications has been added to the solution. With the addition of this module, the total configuration of the equipment began to be performed by Bluetooth. The addition of this module also provided the integration of an Android application to configure the equipment by Bluetooth. The same App is used to present the data sent by the equipment via SMS.

The following image shows the equipment with version 0.6. In this version most components were transferred to the base board except for the microcontroller, GSM and GPS modules. This version already includes a Bluetooth module.

![Trackbees v0.6 board](/assets/blog/2020-12-03-patri-monitoring-hives-post4-test-with-bees-colony-v06.png "Trackbees v0.6 board")
<!--<img src="/assets/blog/2020-12-03-patri-monitoring-hives-post4-test-with-bees-colony-v06.png" width="350px">-->

Next post: integration of BLE (Bluetooth Low Energy) module in TrackBees equipment.

