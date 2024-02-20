# MQTT Authentication for Device Control Commands

To ensure secure and authorized access to devices through MQTT, it is important to implement authentication mechanisms. Here is an example of how you can authenticate MQTT commands that control devices:

## Broker Auth
Before you control a device you must make a successfull connection to the mqtt broker using / creating an mqtt client.

To do this you will need the following auth info:

```json
var options = {
    port: <port number>,
    host: <hostname>,
    clientId: '<random_client_id>', 
    username: '<username>',
    password: '<password>',
    keepalive: 60 (optional),
    reconnectPeriod: 1000 (optional),
    protocolId: 'MQIsdp' (optional),
    protocolVersion: 3 (optional),
    clean: true (optional),
    encoding: 'utf8 (optional)'
};
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

You do that by sending this auth object **ALONG** with the downlink payload


Then you will get the following series of topic responses back immediatly after sending a good command

```mqtt
downlink_response/{property_id}/{source_application_token}/{qr}/{dev_eui}/{response}
```
Where {response} can be any of the following 

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