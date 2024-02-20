# Thermostat Control MQTT Topics

## Introduction

This document provides an overview of the MQTT topics used to send commands that control thermostats. MQTT (Message Queuing Telemetry Transport) is a lightweight messaging protocol commonly used in IoT (Internet of Things) applications.

## Topic Structure

The MQTT topics for thermostat control follow a specific structure to ensure effective communication between the control system and the thermostats. The topics are organized as follows:

## Downlinks


### Set Mode
"command" : "set_mode"
"payload" : { "mode" : "heat|cool|off"}

### Set Schedule Mode
"command" : "set_schedule_mode"
"payload" : { "schedule_mode" : "permanent|temporary|program|vacation" }

### Set Transmit Interval
"command" : "set_tx_interval"
"paylaod" : { "health_seconds" : [30,9000] , "commodity_seconds" : [30,9000] }

### Set Fan Mode
"command" : "set_fan_mode"
"payload" : { "fan_mode" : "on|auto|intermittent|followprogram" }

### Set Set Point
"command" : "set_set_point"
"payload" : { "mode" : "heat|cool", "temperature_f" : [35,100] }

### Set Override 
"command" : "set_override"
"payload" : { "override" : "clear|heat_on|heat_off" }