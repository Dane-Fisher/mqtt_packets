# Thermostat Control MQTT Topics

## Introduction

This document provides an overview of the MQTT topics used to send commands that control thermostats. MQTT (Message Queuing Telemetry Transport) is a lightweight messaging protocol commonly used in IoT (Internet of Things) applications.

## Message Structure

The MQTT Messages for thermostat control follow a specific structure to ensure effective communication between the control system and the thermostats. The topics are organized as follows:

## Related QRs
```json
[92, 105, 36, 33, 34, 35, 67, 1001, 1006, 1009]
```

## Related Uplink Responses
```json
[[179](../responsePackets/zigbee.thermostat.md),129,171,42]
```
## Downlink Commands

### Ping
```json
"allowedQr": [92, 105, 36, 33, 34, 35, 67, 1001, 1006, 1009],
"command" : "ping"
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

### Set Mode
```json
"allowedQr": [92, 105, 36, 33, 34, 35, 67, 1001, 1006, 1009],
"command" : "set_mode"
"payload" : { "mode" : "heat|cool|off"}
```
```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "command": {
      "type": "string",
      "enum": ["set_mode"]
    },
    "payload": {
      "type": "object",
      "properties": {
        "mode": {
          "type": "string",
          "enum": ["heat", "cool", "off"]
        }
      },
      "required": ["mode"]
    }
  },
  "required": ["command", "payload"]
}
```

### Set Schedule Mode
```json
"allowedQr": [92, 105],
"command" : "set_schedule_mode"
"payload" : { "schedule_mode" : "permanent|temporary|program|vacation" }
```
```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "command": {
      "type": "string",
      "enum": ["set_schedule_mode"]
    },
    "payload": {
      "type": "object",
      "properties": {
        "schedule_mode": {
          "type": "string",
          "enum": ["permanent", "temporary", "program", "vacation"]
        }
      },
      "required": ["schedule_mode"]
    }
  },
  "required": ["command", "payload"]
}
```


### Set Transmit Interval
```json
"allowedQr": [92, 105, 36, 33, 34, 35, 67, 1001, 1006, 1009],
"command" : "set_tx_interval"
"paylaod" : { "health_seconds" : [30,9000] , "commodity_seconds" : [30,9000] }
```

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "command": {
      "type": "string",
      "enum": ["set_tx_interval"]
    },
    "payload": {
      "type": "object",
      "properties": {
        "health_seconds": {
          "type": "array",
          "items": {
            "type": "integer",
            "minimum": 30,
            "maximum": 9000
          },
          "minItems": 2,
          "maxItems": 2
        },
        "commodity_seconds": {
          "type": "array",
          "items": {
            "type": "integer",
            "minimum": 30,
            "maximum": 9000
          },
          "minItems": 2,
          "maxItems": 2
        }
      },
      "required": ["health_seconds", "commodity_seconds"]
    }
  },
  "required": ["command", "payload"]
}
```

### Set Fan Mode
```json
"allowedQr": [92, 105, 36, 33, 34, 35, 67, 1001, 1006, 1009],
"command" : "set_fan_mode"
"payload" : { "fan_mode" : "on|auto|intermittent|followprogram" }
```
```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "command": {
      "type": "string",
      "enum": ["set_fan_mode"]
    },
    "payload": {
      "type": "object",
      "properties": {
        "fan_mode": {
          "type": "string",
          "enum": ["on", "auto", "intermittent", "followprogram"]
        }
      },
      "required": ["fan_mode"]
    }
  },
  "required": ["command", "payload"]
}
```

### Set Set Point
```json
"allowedQr": [92, 105, 36, 33, 34, 35, 67, 1001, 1006, 1009],
"command" : "set_set_point"
"payload" : { "mode" : "heat|cool", "temperature_f" : [35,100] }
```

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "command": {
      "type": "string",
      "enum": ["set_set_point"]
    },
    "payload": {
      "type": "object",
      "properties": {
        "mode": {
          "type": "string",
          "enum": ["heat", "cool"]
        },
        "temperature_f": {
          "type": "array",
          "items": {
            "type": "integer",
            "minimum": 35,
            "maximum": 100
          },
          "minItems": 2,
          "maxItems": 2
        }
      },
      "required": ["mode", "temperature_f"]
    }
  },
  "required": ["command", "payload"]
}
```

### Get Zone Settings
```json
"allowedQr": [105, 36],
"command" : "get_zone_settings"
"payload" : {}
```

```json 
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "command": {
      "type": "string"
    },
    "payload": {
      "type": "object"
    }
  },
  "required": ["command", "payload"]
}
```

### Set Zone Settings

2 zones (2 points in the day)  1 master schdeule for the week

```json
"allowedQr":[105,36],
"command" : "set_zone_settings",
"payload" : {  
                    "zone_1_hour_24hr" : 5,
                    "zone_1_minute": 13,
                    "zone_1_set_point_f" : 64,
                    "zone_1_set_limit_f" : 73,
                    "zone_2_hour_24hr" : 21,
                    "zone_2_minute" : 14,
                    "zone_2_set_point_f" : 65,
                    "zone_2_set_limit_f" : 75
                    } 
```

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "command": {
      "type": "string"
    },
    "payload": {
      "type": "object",
      "properties": {
        "zone_1_hour_24hr": { "type": "integer" },
        "zone_1_minute": { "type": "integer" },
        "zone_1_set_point_f": { "type": "integer" },
        "zone_1_set_limit_f": { "type": "integer" },
        "zone_2_hour_24hr": { "type": "integer" },
        "zone_2_minute": { "type": "integer" },
        "zone_2_set_point_f": { "type": "integer" },
        "zone_2_set_limit_f": { "type": "integer" }
      },
      "required": [
        "zone_1_hour_24hr",
        "zone_1_minute",
        "zone_1_set_point_f",
        "zone_1_set_limit_f",
        "zone_2_hour_24hr",
        "zone_2_minute",
        "zone_2_set_point_f",
        "zone_2_set_limit_f"
      ]
    }
  },
  "required": ["command", "payload"]
}
```








