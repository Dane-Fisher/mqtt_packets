```javascript

{
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "transmit_attempt_count": 16469, 
        "pulse_count_raw": 4, 
        "battery_vdc_millivolts": 3590
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
            "device_address": "44E6241E", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "07003C04", 
                    "GatewayRSSI": "-107.000000", 
                    "GatewaySNR": "6.500000", 
                    "GatewayESP": "-107.877357"
                }
            ], 
            "raw_packet": "00001af3000000049f4055", 
            "gateway_snr": 6.5, 
            "bridge_decoder": 46, 
            "frame_count_downlink": 2912, 
            "spreading_factor": 8, 
            "lns_late_bit": 0, 
            "rssi": -107.0, 
            "decoder_type": "", 
            "message_type": 2, 
            "port": 140, 
            "channel": 7, 
            "frame_count_uplink": 16449
        }, 
        "common": {
            "gateway_timestamp": "2023-08-18T16:43:29.103Z", 
            "payload_type": "commodity", 
            "device_type": "pulse_meter", 
            "serial_number": "0004A30B0025F267-2", 
            "firmware_version": "0.0", 
            "gateway_hostname": "0202000007003C04"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_717"
}

```
