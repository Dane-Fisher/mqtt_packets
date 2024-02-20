# Overview
H2o Degree uses MQTT as its main data flow pipeline. Devices like thermostats, water meters and humidity sensors all emit data, receive commands and have configurations. This is all controlled by a system comprised of applications, gateways, workers, and databases. To keep it all organized H2o Engineering has created a general structure to utilize all functions of every supported device. This Document will use a top down approach to describe this structure.

The top of the tree starts with the specific Device. This is in refence to a speicific item with a unique part number. For example T-1000 Thermostat. From the specific device, other properties are derrived. The schema follows this structure: 

**QR Index**|**QR**|**JSON QR Index**|**Part Number**|**Description**|**Unit Code**|**Battery Powered**|**Suffix Req**|**Pulse Channels**
:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:
1000|qr1000|1000|M53120|Water Meter|36|0|0|0
1001|qr1001|1001|M53122|Water Meter|36|0|0|0
1002|qr1002|1002|None|None|36|0|0|0
1003|qr1003|1003|Virtual Offset Device|Virtual Device|36|0|0|0
1004|qr1004|1004|M50441|Water Meter|40|0|0|0
1005|qr1005|1005|M53120-S|Water Meter|42|0|0|0
1006|qr1006|1006|M53450-HPH|Thermostat|42|0|0|0
1007|qr1007|1007|M53200|Router|100|0|0|0
1008|qr1008|1008|M53170|Coordinator|140|0|0|0
1009|qr1009|1009|M52450-HPH|Thermostat|129|0|0|0
1010|qr1010|1010|M53110|Temp and Humid|155|0|0|0
1011|qr1011|1011|M53130|Pulse|140|0|0|0
1012|qr1012|1012|EM1004|EKM Electric|166|0|0|0
1013|qr1013|1013|M54111|Temp Sensor|172|0|0|0
1014|qr1014|1014|Various|Legacy|100|0|0|0
1015|qr1015|1015|M53200-I|Router|100|0|0|0
1016|qr1016|1016|TW1000|Line Powered Tehama|140|0|1|4
1017|qr1017|1017|TW2000|Battery Powered Tehama|140|1|1|4
1018|qr1018|1018|TW-101R-5|Tehama Repeater|100|0|0|0
57|qr57|57|Eaton|Electric Meter|187|0|0|0
40|qr40|40|EM700012S|Electric Meter|187|0|0|0
101|qr101|101|LS8000-ACCU|LoRa Accu KWH Meter|140|0|1|0
102|qr102|102|LS8000-SATC|LoRa Satec KWH Meter|140|0|1|18
76|qr76|76|LEM700012S|LoRa Electric Meter|140|0|0|0
103|qr103|103|LEM70002S|LoRa Electric Meter|140|0|0|0
41|qr41|41|EM700016S|Electric Meter|187|0|0|0
62|qr62|62|EM700016SD|Electric Meter|187|0|0|0
52|qr52|52|HCB0104|Bridge Board|129|0|0|0
89|qr89|89|HCT0104|Thermostat|179|0|0|0
51|qr51|51|HCV0104|Radiator Valve|198|1|0|0
47|qr47|47|IT1000|Nohrtec Gateway|254|0|0|0
68|qr68|68|IT1000-HA|Salus Gateway|254|0|0|0
48|qr48|48|IT1002|Pogo Gateway|254|0|0|0
66|qr66|66|IT1003|Salus Gateway|254|0|0|0
97|qr97|97|IT1004|RPi Gateway|254|0|0|0
53|qr53|53|LIT1005|LoRa Gateway Cell|252|0|0|0
90|qr90|90|LIT1004-MQ|LoRa Gatway Ethernet|252|0|0|0
91|qr91|91|LIT1004-KO|LoRa Gatway Ethernet|252|0|0|0
58|qr58|58|LIT1006|LoRa Gateway Tek|252|0|0|0
84|qr84|84|L54190|LoRa Encoded X|140|1|0|1
86|qr86|86|L54290|LoRa Encoded Pit|140|1|0|1
1|qr1|1|L54230-Tind|LoRa Pulse|140|1|1|2
43|qr43|43|L54230|LoRa Pulse|140|1|1|2
111|qr111|111|WM 2105 H|Hot QEncoded .75|140|1|0|0
106|qr106|106|WM 2105 C|Cold QEncoded .75|140|1|0|0
107|qr107|107|WM 1900 C075|Cold QEncoded .75|140|1|0|0
108|qr108|108|WM 1900 H075|Hot QEncoded .75|140|1|0|0
96|qr96|96|WM-U1100-C075|LoRa Ultra|140|1|0|1
73|qr73|73|L54215|LoRa Single Pulse|140|1|1|1
98|qr98|98|AXIOMA-W1|Ultrasonic Three Quarter|140|1|1|1
110|qr110|110|L54240-RQ-2-H-0|Dragino Wet Pulse|140|0|1|2
104|qr104|104|L54240|Dragino Dry Pulse|140|1|1|2
78|qr78|78|L54215-O|LoRa Single Pulse|140|1|1|1
74|qr74|74|L54215-OTS|LoRa Single Pulse|140|1|1|1
46|qr46|46|L54230|LoRa Pulse|140|1|1|2
81|qr81|81|L54230-O|LoRa Pulse|140|1|1|2
59|qr59|59|L54230-Ots|LoRa Pulse|140|1|1|2
93|qr93|93|L54230-Ots-O|LoRa Pulse Outdoor|140|1|1|2
60|qr60|60|L54110|Lora Climate Sensor|155|1|0|0
85|qr85|85|LS2000-MS|Lora Multi Sensor|1085|1|0|0
79|qr79|79|LS4000-DL|2ch Flood Sensor|1079|1|1|0
82|qr82|82|LS5000-CR|Rope Flood Sensor|1082|1|0|0
80|qr80|80|LS6000-SOV-075|Shut Off Valve|1080|1|0|0
94|qr94|94|LS6000-SOV-075-A|Shut Off W Alarm|1094|1|0|0
95|qr95|95|LS6000-SOV-075-LA|Shut Off W Alarm Local|1095|1|0|0
87|qr87|87|LS6000-SOV-075-CH1|Strega Pulse|140|0|1|1
64|qr64|64|L54110T|Lora Climate Sensor|155|1|0|0
22|qr22|22|M54110|Zigbee Climate Sensor|155|0|0|0
75|qr75|75|L54120+|LoRa Water Meter +|42|1|0|0
99|qr99|99|L54122-OTS|LoRa Water Meter +|42|0|0|0
100|qr100|100|L54120-OTS|LoRa Water Meter +|42|0|0|0
2|qr2|2|M54120+|Water Meter+|42|1|0|0
4|qr4|4|M54120|Water Meter|42|1|0|0
3|qr3|3|M54120-S|Water Meter|42|1|0|0
44|qr44|44|M54120-S+|Water Meter+|42|1|0|0
26|qr26|26|M54122|Water Meter|36|0|0|0
28|qr28|28|M54122+|Water Meter +|36|0|0|0
27|qr27|27|M54122-PS|Water Meter|36|0|0|0
29|qr29|29|M54122-PS+|Water Meter+|36|0|0|0
21|qr21|21|M54130|Pulse|140|0|1|4
14|qr14|14|M54131|BTU 1/2 In|173|0|0|0
54|qr54|54|M54141|WS-BTU 1/2 In|173|0|0|0
55|qr55|55|M54143|WS-BTU 3/4 In|173|0|0|0
15|qr15|15|M54131-TS|BTU 1/2 In|173|0|0|0
13|qr13|13|M54132|BTU 1 In|173|0|0|0
50|qr50|50|M54133|BTU 3/4 In|173|0|0|0
20|qr20|20|M54170|Electric Mtr|140|0|1|1
83|qr83|83|L54170|LoRa Electric Mtr|140|0|1|1
19|qr19|19|M54170-RP|Electric Mtr|140|0|1|2
18|qr18|18|M54170-TP|Electric Mtr|140|0|1|1
31|qr31|31|M54190|Encoded Register|183|0|0|0
32|qr32|32|M54191|Encoded Register|186|0|0|0
5|qr5|5|M54200-RM|Router|100|0|0|0
6|qr6|6|M54200-SI|Router|100|0|0|0
7|qr7|7|M54200-E-110|Router|100|0|0|0
61|qr61|61|M54200-E-277|Router|100|0|0|0
56|qr56|56|M54200-ION|Router|100|0|0|0
8|qr8|8|M54200-O|Outdoor Router|100|0|0|0
9|qr9|9|M54200|Router|100|0|0|0
10|qr10|10|M54200-24|Router|100|0|0|0
30|qr30|30|M54222|1 In Water Mtr|190|0|0|0
17|qr17|17|M54230|Battery Pulse|140|1|1|2
16|qr16|16|M54230-O|Battery Pulse|140|1|1|2
92|qr92|92|T1000|Kono TStat|129|0|0|0
105|qr105|105|T1001|Kono TStat Ctrl|179|0|0|0
33|qr33|33|M54450-HP|Thermostat|129|0|0|0
34|qr34|34|M54450-HPH|Thermostat|129|0|0|0
72|qr72|72|M54450-HA|Salus Thermostat|129|0|0|0
36|qr36|36|M54450-MIN|Thermostat|179|0|0|0
35|qr35|35|M54451-HPH|Thermostat|129|0|0|0
67|qr67|67|M54451-HPH|Thermostat|129|0|0|0
88|qr88|88|M54452-HCB|Thermostat|129|0|0|0
24|qr24|24|M54550|EKM Meter|166|0|1|0
25|qr25|25|M54556|AccuEnergy Electric|140|0|1|20
109|qr109|109|M54560|AccuRev Electric|140|0|1|20
23|qr23|23|M54557|Satec Electric|140|0|1|18
65|qr65|65|M54559|BTU Meter RS485|173|0|0|0
11|qr11|11|M54700-WS|Coordinator|105|0|0|0
12|qr12|12|M54700|Coordinator|105|0|0|0
69|qr69|69|RDU-1000-HC1:10|Remote Dislay Unit|0|0|0|0
70|qr70|70|RDU-1000-C1:7.48|Remote Dislay Unit|0|0|0|0
71|qr71|71|RDU-1000-H1:7.48-C1:1|Remote Dislay Unit|0|0|0|0
37|qr37|37|W54450-MIN|Mini|176|0|0|0
38|qr38|38|W54450-MIN-208|Mini 208|176|0|0|0
77|qr77|77|W54450-HA|Salus Mini|176|0|0|0
39|qr39|39|W54455-MIN|Mini|176|0|0|0
63|qr63|63|W54600|Mini High Load|188|0|0|0
45|qr45|45|VG7000|Vision Gateway|253|0|0|0
49|qr49|49|VRF1000|LG Modbus Controller|187|0|0|0