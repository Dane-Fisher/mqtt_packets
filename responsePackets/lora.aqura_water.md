```javascript {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "transmit_attempt_count": 6885, 
        "gallons": 3858.86, 
        "flow_time_minutes": 3841, 
        "battery_vdc_millivolts": 3652, 
        "flow_events": 2694
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
    "packet_creation_timestamp": 1692377009, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "45F014A4", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "070059F4", 
                    "GatewayRSSI": "-106.000000", 
                    "GatewaySNR": "-3.000000", 
                    "GatewayESP": "-110.764351"
                }
            ], 
            "raw_packet": "00000f12dc0a860f011ae5", 
            "gateway_snr": -3.0, 
            "bridge_decoder": 75, 
            "frame_count_downlink": 25, 
            "spreading_factor": 10, 
            "lns_late_bit": 0, 
            "rssi": -106.0, 
            "decoder_type": "Unknown", 
            "message_type": 4, 
            "port": 210, 
            "channel": 0, 
            "frame_count_uplink": 60
        }, 
        "common": {
            "gateway_timestamp": "2023-08-18T16:43:29.285Z", 
            "payload_type": "commodity", 
            "device_type": "aqura_water", 
            "serial_number": "001DB9DE000014DC", 
            "firmware_version": "0.04", 
            "gateway_hostname": "02020000070059F4"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_717"
}

```
