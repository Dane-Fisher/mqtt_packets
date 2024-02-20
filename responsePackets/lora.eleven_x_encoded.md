```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "valid_read": "yes", 
        "raw_encoded_register": 30501
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
    "packet_creation_timestamp": 1698690175, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "44A83A34", 
            "gateway_count": 2, 
            "gateway_list": [
                {
                    "GatewayID": "0700C6C0", 
                    "GatewayRSSI": "-73.000000", 
                    "GatewaySNR": "11.250000", 
                    "GatewayESP": "-73.314041"
                }, 
                {
                    "GatewayID": "0700A1AE", 
                    "GatewayRSSI": "-109.000000", 
                    "GatewaySNR": "-2.500000", 
                    "GatewayESP": "-113.437759"
                }
            ], 
            "raw_packet": "ab420000007725850100eb", 
            "gateway_snr": 11.25, 
            "bridge_decoder": 84, 
            "frame_count_downlink": 2011, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -73.0, 
            "decoder_type": "Unknown", 
            "message_type": 4, 
            "port": 4, 
            "channel": 4, 
            "frame_count_uplink": 2006
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:22:54.924Z", 
            "payload_type": "commodity", 
            "device_type": "eleven_x_encoded", 
            "serial_number": "70B3B514900B05D1", 
            "firmware_version": "0.0", 
            "gateway_hostname": "020200000700C6C0"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```