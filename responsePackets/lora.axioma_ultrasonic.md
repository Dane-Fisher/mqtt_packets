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
    "packet_creation_timestamp": 1698690094, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "45385EB1", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "07001C39", 
                    "GatewayRSSI": "-52.000000", 
                    "GatewaySNR": "11.750000", 
                    "GatewayESP": "-52.280972"
                }
            ], 
            "raw_packet": "70f53f6510fb070000301c3f65fb070000000000000000000000000000000000000000000000000000000000000000", 
            "gateway_snr": 11.75, 
            "bridge_decoder": 96, 
            "frame_count_downlink": 1723, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -52.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 100, 
            "channel": 7, 
            "frame_count_uplink": 10607
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:21:33.512Z", 
            "payload_type": "commodity", 
            "device_type": "axioma_ultrasonic", 
            "serial_number": "000709000050B302-1", 
            "firmware_version": "0.0", 
            "gateway_hostname": "0202000007001C39"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```