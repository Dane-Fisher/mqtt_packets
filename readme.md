# Overview
H2o Degree uses MQTT as its main data flow pipeline. Devices like thermostats, water meters and humidity sensors all emit data, receive commands and have configurations. This is all controlled by a system comprised of applications, gateways, workers, and databases. To communicate with each other in a standardized way, mqtt messages in the form of downlinks (commands) and uplinks (responses) are used. They are nothing more than normal mqtt messages in the sense that they have a topic and a message part. Where they differ is in what the topic and message contain.

This Repo will organize the devices supported by H2o Degree in the table below, and show the downlinks and uplinks for each. This will in turn will hopefully give you everything you need to know about interacting with a device on an application level.


## Authentication
Since the mqtt data passed back and forth is sensitive data, it is protected by an authentication flow. This flow is in the downlink direction - this means that the downlink commands your application sends will go through an auth server before getting any further down the pipe to a device. At a overview level, the [auth json structure](auth/auth.md) you provide will be concatenated with the commmand payload you send (see docs in table). A series of messages will be published regarding the state upon receival from the auth server. 

**Read more about auth here:** 
[Authentication](auth/auth.md)

## Device level

Each device supported by h2o degree has a unique qr code to identify it. This qr code is representive of the make, model, unitcode, sensor type, radio type, etc of the specific device. The Qr of a device is then related to a unit code response as well as the available commands. Many Qrs will share simmilar commands and responses, however not all of them do. To keep track, the device table below will show which qrs have which unit codes and the available commands. The table is uniquely identified by qr but grouped by general device type (ie thermostat). 

Click the link in the docs column to learn more about the device, its available commands (downlinks) and the response you will get back (unit code)


**Note:**
Currently these are the Devices known to siteManager 2.0

**QR Index**|**QR**|**JSON QR Index**|**Part Number**|**Description**|**Unit Code**|**Docs**|
:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
1006|qr1006|1006|M53450-HPH|Thermostat|42|[Thermostat](devices/thermostats.md)|
1009|qr1009|1009|M52450-HPH|Thermostat|129|[Thermostat](devices/thermostats.md)|
92|qr92|92|T1000|Kono TStat|129|[Thermostat](devices/thermostats.md)|
105|qr105|105|T1001|Kono TStat Ctrl|179|[Thermostat](devices/thermostats.md)|
33|qr33|33|M54450-HP|Thermostat|129|[Thermostat](devices/thermostats.md)|
34|qr34|34|M54450-HPH|Thermostat|129|[Thermostat](devices/thermostats.md)|
72|qr72|72|M54450-HA|Salus Thermostat|129|[Thermostat](devices/thermostats.md)|
36|qr36|36|M54450-MIN|Thermostat|179|[Thermostat](devices/thermostats.md)|
35|qr35|35|M54451-HPH|Thermostat|129|[Thermostat](devices/thermostats.md)|
67|qr67|67|M54451-HPH|Thermostat|129|[Thermostat](devices/thermostats.md)|
88|qr88|88|M54452-HCB|Thermostat|129|[Thermostat](devices/thermostats.md)|
37|qr37|37|W54450-MIN|Mini|176|[Mini](devices/minis.md)|
38|qr38|38|W54450-MIN-208|Mini 208|176|[Mini](devices/minis.md)|
77|qr77|77|W54450-HA|Salus Mini|176|[Mini](devices/minis.md)|
39|qr39|39|W54455-MIN|Mini|176|[Mini](devices/minis.md)|
63|qr63|63|W54600|Mini High Load|188|[Mini](devices/minis.md)|

