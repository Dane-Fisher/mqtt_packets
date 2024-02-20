# Mini devices

## Introduction

This document provides an overview of the MQTT topics used to send commands that control minis. MQTT (Message Queuing Telemetry Transport) is a lightweight messaging protocol commonly used in IoT (Internet of Things) applications.


## Related QRs
```json
[37, 38, 77, 39, 63]
```
## Related Uplink Responses

[[188](../responsePackets/zigbee.mini.md),[176](../responsePackets/zigbee.mini.md)]


## Downlink Commands

### Ping
```json
"allowedQr": [37, 38, 77, 39, 63],
"command" : "ping",
"payload" : {"jitter" : "true || false"}
```

```json 
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "command": {
      "type": "string",
      "enum": ["ping"]
    },
    "payload": {
      "type": "object",
      "properties": {
        "jitter": {
          "type": "boolean"
        }
      },
      "required": ["jitter"]
    }
  },
  "required": ["command", "payload"]
}
```

### Set Override 
```json
"allowedQr" : [37, 38, 77, 39, 63],
"command" : "set_override",
"payload" : { "override" : "clear|heat_on|heat_off" }
```

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "command": {
      "type": "string",
      "enum": ["set_override"]
    },
    "payload": {
      "type": "object",
      "properties": {
        "override": {
          "type": "string",
          "enum": ["clear", "heat_on", "heat_off"]
        }
      },
      "required": ["override"]
    }
  },
  "required": ["command", "payload"]
}
```