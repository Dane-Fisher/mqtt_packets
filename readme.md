# Overview
H2o Degree uses MQTT as its main data flow pipeline. Devices like thermostats, water meters and humidity sensors all emit data, receive commands and have configurations. This is all controlled by a system comprised of applications, gateways, workers, and databases. To keep it all organized H2o Engineering has created a general structure to utilize all functions of every supported device. This Document will use a top down approach to describe this structure.

The top of the tree starts with the specific Device. This is in refence to a speicific item with a unique part number. For example T-1000 Thermostat. From the specific device, other properties are derrived. The schema follows this structure: 

```
Device Name

	Info

	Type

	Commands

		Command Name

			Command Info 

			Request 

				Topic 

				Message

			Response

				Auth Response

				Device Response

	Status Data
		Info 

		response
	
			topic 
	
			message
```



 - The Supporting files in this repo will be every known /  supported H2O Degree device with this tree structure filled out with actual data / descriptions. 




