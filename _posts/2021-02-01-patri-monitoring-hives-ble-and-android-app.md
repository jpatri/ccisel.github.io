---
layout: post
title: Bluetooth module to enhance an Android App
image: 2021-01-06-patri-monitoring-hives-post5-ble-and-android-app_TB_v0.8.png
date: 2021-2-1
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

The Bluetooth Low Energy (BLE) module integration in the equipment enhanced the functional characteristics to a richer and more interesting level than those achieved in previous versions to this integration. This integration also motivated the development of an Android App.that revolutionized the interaction with the equipment. This post presents the integration result of this module in terms of hardware and the interaction achieved with Android App.

## Motivation

[The experience carried out in real environment](https://cc.isel.pt/embedded%20systems/2020/12/20/patri-monitoring-hives-test-with-bees-colony/) demonstrated the relevance of being able to configure the equipment remotely, that is, to have the ability to establish a short distance and wireless connection between the equipment and the device that configures it. The device that configures the equipment corresponds to a mobile phone that is paired with the equipment at an early stage of configuration. The technology selected to establish a short distance and wireless connection was the Bluetooth technology, more specifically Bluetooth Low Energy (BLE).

This technology has been selected because it is present in most smartphones, communicates by radio frequency not requiring the equipment to be in line of view, supports connections up to 10 meters and is low consumption. Other technologies, such as Near Field Connection (NFC), Infrared or WIFI, conditionate the desired operability in different aspects. NFC technology requires a proximity of less than 1 meter, infrared requires that the equipment be in line of view and WIFI imposes a higher consumption than the consumption imposed with the BLE not introducing any additional advantage (assuming a direct connection between the equipment and the smartphone).

## Hardware solution

The first TrackBees board to have integrated a BLE module was the V0.3 version, designed in August 2015. It used the [BLE112 module](https://www.silabs.com/wireless/bluetooth/bluegiga-low-energy-legacy-modules/device.ble112) from Silicon Labs (at the time, that module implemented the BLE4.0 specification). From version V0.8 (October 2017) to the last developed version has been used the [HM-10 module](http://jnhuamao.cn/bluetooth.asp?id=1) from Jinan Huamao Technology. The figures below present two versions, V0.4 and V0.8, each one with their respective BLE module highlighted (for illustration purposes, the microcontroller, GSM and GNSS modules are not mounted).

![Trackbees v0.4 board](/assets/blog/2021-01-06-patri-monitoring-hives-post5-ble-and-android-app_TB_v0.4.png "Trackbees v0.4 board")![Trackbees v0.8 board](/assets/blog/2021-01-06-patri-monitoring-hives-post5-ble-and-android-app_TB_v0.8.png "Trackbees v0.8 board")

[TrackBees solution consists of two subsystems](https://cc.isel.pt/embedded%20systems/2020/10/16/patri-monitoring-hives-battery-charge/) independently powered. The BLE module power is configured by a mechanical switch for subsystem one or subsystem two.

In subsystem one, the BLE module remains powered and, like the accelerometer and real time clock (RTC), may establish power supply of subsystem two. In the case of the BLE module, the power of subsystem two is established when a connection is made with the paired phone.

When powered into subsystem two, it is a component that plays a decisive role in interpreting the power activation of subsystem two: even if power was caused by the RTC or accelerometer, it corresponds to a configuration session if, during the control system initiation, a connection is established with the paired phone, otherwise it corresponds to a monitoring or a theft detection session.

Even if the BLE module power is managed by switch, it is expected that the usual configuration will be in subsystem two because of consumption reasons. Powering in subsystem one is essentially used to define first settings, testing purposes and other applications where autonomy is not a fundamental goal as it is in beehive application.

## Android App

![System generic view](/assets/blog/2021-01-06-patri-monitoring-hives-post5-ble-and-android-app-system-communication.png "System generic view")

The BLE module integration in the equipment motivated the development of an [Android App](https://github.com/jpatri/GuardTracker). The first version of this App was developed during 2016. The Android App allows you to pair your phone with the equipment and configure it, both under BLE connections. The App also presents the data collected by the equipment in monitoring cycles and tracking sessions, received via SMS messages.

Initial pairing ensures that in the future the equipment only establishes Bluetooth connections with the paired phone. Along with this process, it is defined the phone contact to where the equipment must send SMS messages. After, you may change this contact and add a maximum of three different numbers. All defined contacts receive SMS messages.

The data received by SMS of a monitoring cycle corresponds so far to geographic position, battery charge, SIM card balance and temperature. This data is stored in the App in a database and presented by category. The geographical positions are displayed on a map and the other information is displayed in chart form (credits for [MPAndroidChart](https://weeklycoding.com/mpandroidchart-documentation/)). At the time of writing this post, I have no examples of these screens.

The following images illustrate the current version of the App main page (with no paired equipment). The main page is divided into different sections, namely, identification of the equipment, current state, settings edition area, contacts and history.

![Android App main page - Id and current state](/assets/blog/2021-01-06-patri-monitoring-hives-post5-ble-and-android-app_main1.png "Android App main page - Id and current state")  ![Android App main page - Settings edition area](/assets/blog/2021-01-06-patri-monitoring-hives-post5-ble-and-android-app_main2.png "Android App main page - Settings edition area")  ![Android App main page - Contacts and history](/assets/blog/2021-01-06-patri-monitoring-hives-post5-ble-and-android-app_main3.png "Android App main page  - Contacts and history")
<!--<img src="/assets/blog/2020-12-03-patri-monitoring-hives-post4-test-with-bees-colony-v06.png" width="350px">-->

The Android App lets you configure several equipment settings. These may be done offline and become pending until they are synced via bluetooth to the equipment. Android App allows you to:

* Modify equipment reference position
* Define which sensors may enable power supply of subsystem two (BLE, RTC and accelerometer)
* Configure settings related to monitoring, tracking, and surveillance

The ability to configure sensor activation, namely, the accelerometer, is of great help to install the equipment in the beehive since we can handle the equipment freely without starting a theft detection session.

The images below display the views to inspect and edit monitoring, tracking, and surveillance settings.

![Monitorization screen](/assets/blog/2021-01-06-patri-monitoring-hives-post5-ble-and-android-app_mon.png "Monitorization screen")  ![Tracking screen](/assets/blog/2021-01-06-patri-monitoring-hives-post5-ble-and-android-app_track.png "Tracking screen")  ![Surveillance screen](/assets/blog/2021-01-06-patri-monitoring-hives-post5-ble-and-android-app_vig.png "Surveillance screen")

At the monitoring level you may configure:

* The time of day to perform a monitoring cycle
* The period based on the time settled above to perform a monitoring session
* The criteria for sending SMS messages
* The minimum difference from the current geographical position to the reference position to consider equipment moved
* The minimum number of satellites in view to acquire geographical positions
* The timeout to acquire a valid geographical position
* Valid temperature range.

At the tracking level you may configure:

* The criteria for sending SMS messages
* The minimum distance from the last position registered to consider position modified
* The minimum number of satellites in view to acquire geographical positions
* The timeout to acquire a valid geographical position
* Three timeouts related to tracking sessions. The three timeouts set the maximum time without movement to update the state of the equipment control system. Tracking is divided into three phases: pre-tracking; tracking; and post-tracking. In the first phase, pre-tracking, the system considers an accelerometer false activation if timeout is reached without the equipment modifying its position. In this case, it returns to surveillance mode, silently. In the tracking phase, it is interpreted as stopping the equipment movement forcing the transition to the post-tracking phase. In the post-tracking phase, it returns to the tracking phase again if it gets a position change before timeout, otherwise, the system terminates the tracking session and transits to surveillance mode. In these two last phases, SMS messages are sent to the App with current positions depending on defined settings.

At the surveillance level you may configure:

* The accelerometer sensitivity
* The BLE module advertisement cycle that corresponds to BLE wake up period from sleep mode to try a Bluetooth connection

Surveillance configurations are not yet supported by the device control system.

## Conclusion

The BLE module integration in the equipment and the Android App development made the user interface much more friendly, practical and interesting than the defined before this integration. Before this integration, the solution implemented for equipment pairing and configuring depends on SMS messages sent from the phone. In most cases, the feedback was not immediate providing some concern about operations success. Unlike, with bluetooth connection, feedback becomes immediate and, in addition, avoids the cost with SMS messages. During testing, I often got the feeling I was dealing with a gadget.

Next post: current version of the equipment and future directions.
