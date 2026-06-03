---
name: mqtt-telemetry
description: >
  Lightweight publish/subscribe messaging protocol broker integration.
---

# MQTT Telemetry Interface

## Overview
MQTT (Message Queuing Telemetry Transport) is a lightweight messaging protocol designed for constrained devices and low-bandwidth, high-latency, or unreliable networks. It is the de facto standard for IoT telemetry.

## Common CLI Commands (Mosquitto)
```bash
# Subscribe to a topic
mosquitto_sub -h broker.hivemq.com -t "home/sensor/temp"

# Publish a telemetry message
mosquitto_pub -h broker.hivemq.com -t "home/sensor/temp" -m "22.5"
```

## Python Integration
```python
import paho.mqtt.client as mqtt

def on_connect(client, userdata, flags, rc):
    client.subscribe("home/sensor/temp")

def on_message(client, userdata, msg):
    print(msg.topic + " " + str(msg.payload))

client = mqtt.Client()
client.on_connect = on_connect
client.on_message = on_message
client.connect("broker.hivemq.com", 1883, 60)
client.loop_forever()
```
