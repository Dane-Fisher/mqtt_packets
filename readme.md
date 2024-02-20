# Overview
H2o Degree uses MQTT as its main data flow pipeline. Devices like thermostats, water meters and humidity sensors all emit data, receive commands and have configurations. This is all controlled by a system comprised of applications, gateways, workers, and databases. To communicate with each other in a standardized way, mqtt messages in the form of downlinks (commands) and uplinks (responses) are used. They are nothing more than normal mqtt messages in the sense that they have a topic and a message part. Where they differ is in what the topic and message contain. This Repo will organize the devices supported by H2o Degree in the table below, and show the downlinks and uplinks for each. This will in turn give you everything you need to know about interacting with a device on an application level.

Checkout the uplink commands in response packets directory and checkout the downlink commands in the downlinkPackets directory. 

**Note:**
Currently these are the Devices known to siteManager 2.0

**QR Index**|**QR**|**JSON QR Index**|**Part Number**|**Description**|**Unit Code**|
:-----:|:-----:|:-----:|:-----:|:-----:|:-----:

1006|qr1006|1006|M53450-HPH|Thermostat|42|
1007|qr1007|1007|M53200|Router|100|
1008|qr1008|1008|M53170|Coordinator|140|
1009|qr1009|1009|M52450-HPH|Thermostat|129|
92|qr92|92|T1000|Kono TStat|129|
105|qr105|105|T1001|Kono TStat Ctrl|179|
33|qr33|33|M54450-HP|Thermostat|129|
34|qr34|34|M54450-HPH|Thermostat|129|
72|qr72|72|M54450-HA|Salus Thermostat|129|
36|qr36|36|M54450-MIN|Thermostat|179|
35|qr35|35|M54451-HPH|Thermostat|129|
67|qr67|67|M54451-HPH|Thermostat|129|
88|qr88|88|M54452-HCB|Thermostat|129|
37|qr37|37|W54450-MIN|Mini|176|
38|qr38|38|W54450-MIN-208|Mini 208|176|
77|qr77|77|W54450-HA|Salus Mini|176|
39|qr39|39|W54455-MIN|Mini|176|
63|qr63|63|W54600|Mini High Load|188|

