```javascript

{
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "humidity": 68, 
        "temperature_c": 23.56, 
        "temperature_f": 74.41, 
        "temperature_valid": "yes", 
        "battery_vdc_millivolts": 3600.0, 
        "humidity_valid": "yes"
    }, 
    "location_information": {
        "property_name": "", 
        "attached_to": "", 
        "device_unique_id": 0, 
        "apartment_id": 0, 
        "bathroom_count": 0, 
        "repair_flag_reason": "", 
        "repair_flag": 0, 
        "meter_type": "", 
        "location_information_found": 0, 
        "apartment_name": "", 
        "bedroom_count": 0, 
        "building_id": 0, 
        "property_id": 0, 
        "building_name": ""
    }, 
    "transmission_type": "scheduled", 
    "packet_creation_timestamp": 1692376983, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "45106173", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "070038AA", 
                    "GatewayRSSI": "-101.000000", 
                    "GatewaySNR": "8.750000", 
                    "GatewayESP": "-101.543648"
                }
            ], 
            "raw_packet": "010b012409341ae9000000", 
            "gateway_snr": 8.75, 
            "bridge_decoder": 60, 
            "frame_count_downlink": 2489, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -101.0, 
            "decoder_type": "MQdevice", 
            "message_type": 2, 
            "port": 6, 
            "channel": 0, 
            "frame_count_uplink": 50569
        }, 
        "common": {
            "gateway_timestamp": "2023-08-18T16:43:02.664Z", 
            "payload_type": "commodity", 
            "device_type": "temperature_humidity_sensor", 
            "serial_number": "00137A10000047D0", 
            "firmware_version": "0.0", 
            "gateway_hostname": "02020000070038AA"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_717"
}

```
