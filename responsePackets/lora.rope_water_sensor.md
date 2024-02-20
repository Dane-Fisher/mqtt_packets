```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "battery_vdc_millivolts": 3600, 
        "rope_sensor": 0
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
    "packet_creation_timestamp": 1698690996, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "447341D1", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "07001C39", 
                    "GatewayRSSI": "-55.000000", 
                    "GatewaySNR": "11.500000", 
                    "GatewayESP": "-55.297062"
                }
            ], 
            "raw_packet": "0112012400000000000000", 
            "gateway_snr": 11.5, 
            "bridge_decoder": 82, 
            "frame_count_downlink": 1416, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -55.0, 
            "decoder_type": "MQdevice", 
            "message_type": 2, 
            "port": 6, 
            "channel": 0, 
            "frame_count_uplink": 7110
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:36:36.176Z", 
            "payload_type": "commodity", 
            "device_type": "rope_water_sensor", 
            "serial_number": "00137A100000C09F", 
            "firmware_version": "0.0", 
            "gateway_hostname": "0202000007001C39"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```