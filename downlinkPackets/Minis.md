# Mini devices

## Introduction

This document provides an overview of the MQTT topics used to send commands that control minis. MQTT (Message Queuing Telemetry Transport) is a lightweight messaging protocol commonly used in IoT (Internet of Things) applications.


## Related QRs
[37, 38, 77, 39, 63]

## Related Uplink Responses


## Downlink Commands

### Ping
```json
"allowedQr": [37, 38, 77, 39, 63],
"command" : "ping",
"payload" : {"jitter" : "true || false"}
```

### Set Override 
```json
"allowedQr" : [37, 38, 77, 39, 63],
"command" : "set_override",
"payload" : { "override" : "clear|heat_on|heat_off" }
```