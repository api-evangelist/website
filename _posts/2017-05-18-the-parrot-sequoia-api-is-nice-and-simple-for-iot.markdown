---
title: The Parrot Sequoia API Is Nice And Simple For IoT
date: 2017-05-18 09:00:00 Z
tags:
- Internet of Things
- Sensors
- Cameras
---

<p><a href="http://developer.parrot.com/"><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions/parrot/sequoia-sensor.jpg" align="right" width="35%" /></a></p>
I'm profiling a number of drone APIs lately and I came across some interesting APIs out of [Parrot](http://developer.parrot.com/). Not all of the APIs are for drones, but I thought they were clean and simple examples of what IoT APIs can look like.

[The API for the Parrot Sequoia camera](http://developer.parrot.com/docs/sequoia/) can be controlled over USB, WIFI, allowing you to change settings, calibrate the sensors, trigger image capture and manage memory, and files.

Here are the paths for the device:

* /capture: to get the Sequoia capture state, start and stop a capture
* /config: to get and set the configuration of the camera
* /status: to get all information about the Sequoia physical state
* /calibration: to get the calibration status, start and stop a calibration
* /storage: to get informations about memory
* /file: to get files and folders information
* /download: to download files
* /delete: to delete files and folders
* /version: to get serial number and software version
* /wifi: to get the Sequoia SSID
* /manualmode: to get and set ISO and exposure manually
* /websocket: to use WebSocket notifications on asynchronous events

I like the simple use of API design to express what is possible with an IoT device and that a small hand-held deployable camera and sensor can be defined in this way. While you still need some coding skills to bring any integration life, anyone could land on the API page and pretty quickly understand what is possible with the device API.

When I come across simple approaches to IoT devices using web APIs I try to write about them, adding them to my research when it comes to IoT APIs. It gives me an easy way to find it again in the future, but also hopefully provides IoT manufacturers some examples of how you can do this as simply and effectively as you can.

I need as many examples of how APIs can be in the cloud, or even on a device like the [Parrot Sequoia API](http://developer.parrot.com/docs/sequoia/).