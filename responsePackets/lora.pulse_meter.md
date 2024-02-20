```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "transmit_attempt_count": 22703, 
        "pulse_count_raw": 1, 
        "battery_vdc_millivolts": 3610
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
    "packet_creation_timestamp": 1698690998, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "44B91D86", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "07003F6E", 
                    "GatewayRSSI": "-108.000000", 
                    "GatewaySNR": "-4.000000", 
                    "GatewayESP": "-113.455406"
                }
            ], 
            "raw_packet": "0001ef1000000001a158af", 
            "gateway_snr": -4.0, 
            "bridge_decoder": 46, 
            "frame_count_downlink": 3466, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -108.0, 
            "decoder_type": "", 
            "message_type": 2, 
            "port": 140, 
            "channel": 6, 
            "frame_count_uplink": 22698
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:36:38.092Z", 
            "payload_type": "commodity", 
            "device_type": "pulse_meter", 
            "serial_number": "0004A30B00F91B37-2", 
            "firmware_version": "6.05", 
            "gateway_hostname": "0202000007003F6E"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```