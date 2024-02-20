```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "humidity": 56, 
        "temperature_c": 24.44, 
        "temperature_f": 75.99, 
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
    "packet_creation_timestamp": 1698690988, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "44400717", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "07001C39", 
                    "GatewayRSSI": "-51.000000", 
                    "GatewaySNR": "10.500000", 
                    "GatewayESP": "-51.370777"
                }
            ], 
            "raw_packet": "010b0124098c1616000000", 
            "gateway_snr": 10.5, 
            "bridge_decoder": 60, 
            "frame_count_downlink": 238, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -51.0, 
            "decoder_type": "MQdevice", 
            "message_type": 2, 
            "port": 6, 
            "channel": 1, 
            "frame_count_uplink": 1645
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:36:28.255Z", 
            "payload_type": "commodity", 
            "device_type": "temperature_humidity_sensor", 
            "serial_number": "00137A100000932A", 
            "firmware_version": "0.0", 
            "gateway_hostname": "0202000007001C39"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```