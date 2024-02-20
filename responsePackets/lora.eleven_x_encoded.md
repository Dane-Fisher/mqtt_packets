```javascript

{
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "valid_read": "yes", 
        "raw_encoded_register": 1314
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
    "packet_creation_timestamp": 1692376309, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "458CED86", 
            "gateway_count": 2, 
            "gateway_list": [
                {
                    "GatewayID": "0700C6C0", 
                    "GatewayRSSI": "-105.000000", 
                    "GatewaySNR": "2.500000", 
                    "GatewayESP": "-106.937759"
                }, 
                {
                    "GatewayID": "0700A1AE", 
                    "GatewayRSSI": "-105.000000", 
                    "GatewaySNR": "-4.250000", 
                    "GatewayESP": "-110.635674"
                }
            ], 
            "raw_packet": "76420000000522850100f8", 
            "gateway_snr": 2.5, 
            "bridge_decoder": 84, 
            "frame_count_downlink": 248, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -105.0, 
            "decoder_type": "Unknown", 
            "message_type": 4, 
            "port": 4, 
            "channel": 1, 
            "frame_count_uplink": 243
        }, 
        "common": {
            "gateway_timestamp": "2023-08-18T16:31:49.128Z", 
            "payload_type": "commodity", 
            "device_type": "eleven_x_encoded", 
            "serial_number": "70B3B514900B0659", 
            "firmware_version": "0.0", 
            "gateway_hostname": "020200000700C6C0"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_717"
}

```
