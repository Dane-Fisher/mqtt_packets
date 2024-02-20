# Mini devices

## Introduction

This document provides an overview of the MQTT topics used to send commands that control minis. MQTT (Message Queuing Telemetry Transport) is a lightweight messaging protocol commonly used in IoT (Internet of Things) applications.


## Related QRs
[37, 38, 77, 39, 63]

## Related Uplink Responses


## Downlink Commands

### Ping
"allowedQr": [92, 105, 36, 33, 34, 35, 67, 1001, 1006, 1009],
"command" : "ping"
"payload" : {"jitter" : "true || false"}

### Set Override 
"command" : "set_override"
"payload" : { "override" : "clear|heat_on|heat_off" }