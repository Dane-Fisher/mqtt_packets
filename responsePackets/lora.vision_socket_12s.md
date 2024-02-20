```javascript

{
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "vision_status": "ok", 
        "electric_kwh": 1610
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
    "packet_creation_timestamp": 1692376996, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "45CCFEB0", 
            "gateway_count": 2, 
            "gateway_list": [
                {
                    "GatewayID": "07001770", 
                    "GatewayRSSI": "-83.000000", 
                    "GatewaySNR": "12.500000", 
                    "GatewayESP": "-83.237602"
                }, 
                {
                    "GatewayID": "070020B4", 
                    "GatewayRSSI": "-114.000000", 
                    "GatewaySNR": "-9.000000", 
                    "GatewayESP": "-123.514969"
                }
            ], 
            "raw_packet": "d40325012c500523d320", 
            "gateway_snr": 12.5, 
            "bridge_decoder": 76, 
            "frame_count_downlink": 738, 
            "spreading_factor": 9, 
            "lns_late_bit": 0, 
            "rssi": -83.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 1, 
            "channel": 5, 
            "frame_count_uplink": 8171
        }, 
        "common": {
            "gateway_timestamp": "2023-08-18T16:43:15.851Z", 
            "payload_type": "commodity", 
            "device_type": "vision_socket_12s", 
            "serial_number": "BF3881B1AC66F542", 
            "firmware_version": "0.0", 
            "gateway_hostname": "0202000007001770"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_717"
}

```
