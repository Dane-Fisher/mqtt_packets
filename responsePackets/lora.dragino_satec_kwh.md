```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "packet_count": 15, 
        "modbus_address": 15, 
        "sub_packet_number": 14, 
        "electric_kwh": 0, 
        "modbus_condition_code": 3
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
    "packet_creation_timestamp": 1698690766, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "444C0873", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "070005A0", 
                    "GatewayRSSI": "-117.000000", 
                    "GatewaySNR": "-7.750000", 
                    "GatewayESP": "-125.423981"
                }
            ], 
            "raw_packet": "0f0e0f03040000000015f3", 
            "gateway_snr": -7.75, 
            "bridge_decoder": 102, 
            "frame_count_downlink": 1055, 
            "spreading_factor": 9, 
            "lns_late_bit": 0, 
            "rssi": -117.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 2, 
            "channel": 7, 
            "frame_count_uplink": 13154
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:32:46.228Z", 
            "payload_type": "commodity", 
            "device_type": "dragino_satec_kwh", 
            "serial_number": "A8404106C1873A28-15", 
            "firmware_version": "0.0", 
            "gateway_hostname": "02020000070005A0"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```