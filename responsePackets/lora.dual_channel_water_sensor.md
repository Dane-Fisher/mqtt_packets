```javascript

{
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "sensor_2": 0, 
        "sensor_1": 0, 
        "alarm_sensor": 0, 
        "battery_vdc_millivolts": 3000
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
    "packet_creation_timestamp": 1692376986, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "44BF5063", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "070024F4", 
                    "GatewayRSSI": "-102.000000", 
                    "GatewaySNR": "7.000000", 
                    "GatewayESP": "-102.790100"
                }
            ], 
            "raw_packet": "0106011e00000000000000", 
            "gateway_snr": 7.0, 
            "bridge_decoder": 79, 
            "frame_count_downlink": 1464, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -102.0, 
            "decoder_type": "MQdevice", 
            "message_type": 2, 
            "port": 6, 
            "channel": 0, 
            "frame_count_uplink": 13098
        }, 
        "common": {
            "gateway_timestamp": "2023-08-18T16:43:05.707Z", 
            "payload_type": "commodity", 
            "device_type": "dual_channel_water_sensor", 
            "serial_number": "00137A1000008F7E-2", 
            "firmware_version": "0.0", 
            "gateway_hostname": "02020000070024F4"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_717"
}

```
