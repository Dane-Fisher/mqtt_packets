```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "vision_status": "ok", 
        "electric_kwh": 1601
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
    "packet_creation_timestamp": 1698690955, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "45E874E6", 
            "gateway_count": 3, 
            "gateway_list": [
                {
                    "GatewayID": "070020B4", 
                    "GatewayRSSI": "-33.000000", 
                    "GatewaySNR": "11.500000", 
                    "GatewayESP": "-33.297062"
                }, 
                {
                    "GatewayID": "0700662C", 
                    "GatewayRSSI": "-109.000000", 
                    "GatewaySNR": "3.750000", 
                    "GatewayESP": "-110.528069"
                }, 
                {
                    "GatewayID": "07001770", 
                    "GatewayRSSI": "-111.000000", 
                    "GatewaySNR": "-7.000000", 
                    "GatewayESP": "-118.790100"
                }
            ], 
            "raw_packet": "d403208139780523d350", 
            "gateway_snr": 11.5, 
            "bridge_decoder": 76, 
            "frame_count_downlink": 1085, 
            "spreading_factor": 9, 
            "lns_late_bit": 0, 
            "rssi": -33.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 1, 
            "channel": 7, 
            "frame_count_uplink": 12166
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:35:54.9Z", 
            "payload_type": "commodity", 
            "device_type": "vision_socket_12s", 
            "serial_number": "BE973A8EE0C4CC6D", 
            "firmware_version": "0.0", 
            "gateway_hostname": "02020000070020B4"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```