```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "sensor_2": 0, 
        "sensor_1": 0, 
        "alarm_sensor": 0, 
        "battery_vdc_millivolts": 2900
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
    "packet_creation_timestamp": 1698690953, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "4551C93E", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "070024F4", 
                    "GatewayRSSI": "-87.000000", 
                    "GatewaySNR": "8.250000", 
                    "GatewayESP": "-87.605560"
                }
            ], 
            "raw_packet": "0106011d00000000000000", 
            "gateway_snr": 8.25, 
            "bridge_decoder": 79, 
            "frame_count_downlink": 14, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -87.0, 
            "decoder_type": "MQdevice", 
            "message_type": 2, 
            "port": 6, 
            "channel": 1, 
            "frame_count_uplink": 170
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:35:52.705Z", 
            "payload_type": "commodity", 
            "device_type": "dual_channel_water_sensor", 
            "serial_number": "00137A1000008F25-2", 
            "firmware_version": "0.0", 
            "gateway_hostname": "02020000070024F4"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```