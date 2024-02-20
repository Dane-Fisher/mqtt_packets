# MQTT Authentication for Device Control Commands

To ensure secure and authorized access to devices through MQTT, it is important to implement authentication mechanisms. Here is an example of how you can authenticate MQTT commands that control devices:

## Broker Auth
Before you control a device you must make a successfull connection to the mqtt broker using / creating an mqtt client.

To do this you will need the following auth info:

```json
{
    port: <port number>,
    host: <hostname>,
    clientId: '<random_client_id>', 
    username: '<username>',
    password: '<password>',
    keepalive: 60,
    reconnectPeriod: 1000,
    protocolId: 'MQIsdp',
    protocolVersion: 3,
    clean: true,
    encoding: 'utf8'
}
```

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "port": {
      "type": "integer"
    },
    "host": {
      "type": "string"
    },
    "clientId": {
      "type": "string"
    },
    "username": {
      "type": "string"
    },
    "password": {
      "type": "string"
    },
    "keepalive": {
      "type": "integer",
      "default": 60
    },
    "reconnectPeriod": {
      "type": "integer",
      "default": 1000
    },
    "protocolId": {
      "type": "string",
      "default": "MQIsdp"
    },
    "protocolVersion": {
      "type": "integer",
      "default": 3
    },
    "clean": {
      "type": "boolean",
      "default": true
    },
    "encoding": {
      "type": "string",
      "default": "utf8"
    }
  },
  "required": ["port", "host", "clientId", "username", "password"]
}
```

## Auth server

After connecting to the client, you will have to pass h2o degree downlink authentication flow.

You do that by sending the following auth message object **ALONG** with the downlink_payload (the command) on the following topic:

#### Auth Topic

```mqtt
downlink_auth_request/{source_application_token}
```
Where the source application token is arbitrarly made up for mqtt bus filtering

#### Auth Message

```json
{
                "user_id" : 9
                "target_unique_id" : 368081,
                "sk" : "xxxxxxxxxxxxxxx",
                "target_property_id" : 480,
                "target_dev_eui" : "000D6F0011112222",
                "user_email" : "billw@",
                "target_hostname_list" : [ "0202000007009999","FFFF000010101010","m1058653","royal_oaks" ]
                "qr": 80
                "command" : "set_cool_setpoint"
                "command_token" : "ldf_bwild_portal_tpanel",
                
                "downlink_payload" : { "setpoint'": 53 } 
}
```
```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "user_id": {
      "type": "integer"
    },
    "target_unique_id": {
      "type": "integer"
    },
    "sk": {
      "type": "string"
    },
    "target_property_id": {
      "type": "integer"
    },
    "target_dev_eui": {
      "type": "string"
    },
    "user_email": {
      "type": "string"
    },
    "target_hostname_list": {
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "qr": {
      "type": "integer"
    },
    "command": {
      "type": "string",
      "enum": ["set_cool_setpoint"]
    },
    "command_token": {
      "type": "string"
    },
    "downlink_payload": {
      "type": "object",
      "properties": {
        "setpoint": {
          "type": "integer"
        }
      },
      "required": ["setpoint"]
    }
  },
  "required": ["user_id", "target_unique_id", "sk", "target_property_id", "target_dev_eui", "user_email", "target_hostname_list", "qr", "command", "command_token", "downlink_payload"]
}
```

Then you will get the a series of responses back on the following topics immediatly after sending a properly formed command

```mqtt
downlink_response/{property_id}/{source_application_token}/{qr}/{dev_eui}/{response}
```
*Where {response} can be any of the following* 

 - auth_request_received - ack for the auth request
 - auth_request_accepted 
 - auth_request_rejected
 - downlink_accepted - downlink was received by the target gateway or worker
 - downlink_sent - downlink has been sent 
 - downlink_failed - the downlink was accepted and sent but there was no ack received from the device or a retry has finally failed 
 - downlink_already_in_flight - there is already a pending command being sent to the device
 - downlink_retry - attempting to resend the command
 - downlink_resent - the retry command was submitted 
 - downlink_ack_received - the reply was received from the device . likely the actual packet was already processed. this can be ignored 