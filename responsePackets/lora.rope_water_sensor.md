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
    "packet_creation_timestamp": 1692376960, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "441C6EC1", 
            "gateway_count": 3, 
            "gateway_list": [
                {
                    "GatewayID": "07003BC6", 
                    "GatewayRSSI": "-93.000000", 
                    "GatewaySNR": "9.250000", 
                    "GatewayESP": "-93.487717"
                }, 
                {
                    "GatewayID": "070020E4", 
                    "GatewayRSSI": "-99.000000", 
                    "GatewaySNR": "7.750000", 
                    "GatewayESP": "-99.673981"
                }, 
                {
                    "GatewayID": "07004D8C", 
                    "GatewayRSSI": "-114.000000", 
                    "GatewaySNR": "-6.000000", 
                    "GatewayESP": "-120.973228"
                }
            ], 
            "raw_packet": "0112012400000000000000", 
            "gateway_snr": 9.25, 
            "bridge_decoder": 82, 
            "frame_count_downlink": 101, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -93.0, 
            "decoder_type": "MQdevice", 
            "message_type": 2, 
            "port": 6, 
            "channel": 5, 
            "frame_count_uplink": 300
        }, 
        "common": {
            "gateway_timestamp": "2023-08-18T16:42:40.339Z", 
            "payload_type": "commodity", 
            "device_type": "rope_water_sensor", 
            "serial_number": "00137A100000C0EF", 
            "firmware_version": "0.0", 
            "gateway_hostname": "0202000007003BC6"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_717"
}

```
