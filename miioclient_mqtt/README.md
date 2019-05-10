This is a MQTT client which will connect to the modified miio_client on the gateway.

Requirements:
	pip install paho-mqtt
	

Before running, you need to modify the Python script.

There is a section "Constants" where you need to put the following details:

MQTT_USERNAME: username uses to connecto to your MQTT broker
MQTT_PASSWORD: password for the user
MQTT_PREFIX: prefix of the mqtt topics, ie: "/home/xiaomigateway/"
MQTT_BROKER_IP: the IP of your MQTT borker

MIIO_GATEWAY_IP: the IP of your Xiaomi gateway


Once done, just launch:

	python3 miioclient_mqtt.py

The script will output messages received from the gateway AND messages published on MQTT.

To run in "production", just launch: python3 miioclient_mqtt.py >/dev/null 2>&1
