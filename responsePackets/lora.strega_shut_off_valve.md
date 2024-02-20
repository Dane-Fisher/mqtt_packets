```javascript

{
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "fraud": "yes", 
        "counter_value": 0, 
        "tamper": "no", 
        "valve_position": "open", 
        "device_class": "class_c", 
        "leak": "no", 
        "power_source": "external", 
        "digital_input_1": 0, 
        "digital_input_0": 0, 
        "battery_vdc_millivolts": 3667
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
    "packet_creation_timestamp": 1692377005, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "00F92DB8", 
            "gateway_count": 3, 
            "gateway_list": [
                {
                    "GatewayID": "07003BC6", 
                    "GatewayRSSI": "-73.000000", 
                    "GatewaySNR": "9.500000", 
                    "GatewayESP": "-73.461838"
                }, 
                {
                    "GatewayID": "070020E4", 
                    "GatewayRSSI": "-109.000000", 
                    "GatewaySNR": "3.000000", 
                    "GatewayESP": "-110.764351"
                }, 
                {
                    "GatewayID": "07004D8C", 
                    "GatewayRSSI": "-112.000000", 
                    "GatewaySNR": "-2.750000", 
                    "GatewayESP": "-116.599426"
                }
            ], 
            "raw_packet": "f336363775", 
            "gateway_snr": 9.5, 
            "bridge_decoder": 80, 
            "frame_count_downlink": 2, 
            "spreading_factor": 9, 
            "lns_late_bit": 0, 
            "rssi": -73.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 4, 
            "channel": 2, 
            "frame_count_uplink": 1
        }, 
        "common": {
            "gateway_timestamp": "2023-08-18T16:43:24.74Z", 
            "payload_type": "commodity", 
            "device_type": "strega_shut_off_valve", 
            "serial_number": "0004A30B00F92DB8", 
            "firmware_version": "0.0", 
            "gateway_hostname": "0202000007003BC6"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_717"
}

```
