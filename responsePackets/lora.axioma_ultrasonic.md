```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "dry": "yes", 
        "backflow": "no", 
        "burst": "no", 
        "gallons": 2043, 
        "hardware_error": "no", 
        "leak": "no", 
        "low_temperature": "no", 
        "low_battery": "no"
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
    "transmission_type": "alarm", 
    "packet_creation_timestamp": 1692378512, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "45385EB1", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "07001C39", 
                    "GatewayRSSI": "-55.000000", 
                    "GatewaySNR": "7.500000", 
                    "GatewayESP": "-55.710819"
                }
            ], 
            "raw_packet": "bea6df6410fb070000a0d0de64fb070000000000000000000000000000000000000000000000000000000000000000", 
            "gateway_snr": 7.5, 
            "bridge_decoder": 96, 
            "frame_count_downlink": 997, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -55.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 100, 
            "channel": 2, 
            "frame_count_uplink": 6264
        }, 
        "common": {
            "gateway_timestamp": "2023-08-18T17:08:32.418Z", 
            "payload_type": "commodity", 
            "device_type": "axioma_ultrasonic", 
            "serial_number": "000709000050B302-1", 
            "firmware_version": "0.0", 
            "gateway_hostname": "0202000007001C39"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_717"
} 

```