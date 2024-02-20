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
        "battery_vdc_millivolts": 3648
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
    "packet_creation_timestamp": 1698690978, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "00F94AE5", 
            "gateway_count": 3, 
            "gateway_list": [
                {
                    "GatewayID": "070020E4", 
                    "GatewayRSSI": "-77.000000", 
                    "GatewaySNR": "9.500000", 
                    "GatewayESP": "-77.461838"
                }, 
                {
                    "GatewayID": "07003BC6", 
                    "GatewayRSSI": "-97.000000", 
                    "GatewaySNR": "9.000000", 
                    "GatewayESP": "-97.514969"
                }, 
                {
                    "GatewayID": "07004D8C", 
                    "GatewayRSSI": "-103.000000", 
                    "GatewaySNR": "7.500000", 
                    "GatewayESP": "-103.710815"
                }
            ], 
            "raw_packet": "f336343875", 
            "gateway_snr": 9.5, 
            "bridge_decoder": 80, 
            "frame_count_downlink": 144, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -77.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 4, 
            "channel": 0, 
            "frame_count_uplink": 181
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:36:18.045Z", 
            "payload_type": "commodity", 
            "device_type": "strega_shut_off_valve", 
            "serial_number": "0004A30B00F94AE5", 
            "firmware_version": "0.0", 
            "gateway_hostname": "02020000070020E4"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```