---
name: home-assistant
description: >
  Open source home automation hub prioritizing local privacy.
---

# Home Assistant Local IoT Hub

## Overview
Home Assistant is an open-source home automation system that runs on local servers (like a Raspberry Pi) and acts as the central control processor for smart home devices.

## REST API Integration
Home Assistant exposes RESTful endpoints for telemetry status and actions.
- **Retrieve entity state**: `GET http://<IP>:8123/api/states/light.living_room`
- **Trigger service (turn light on)**: `POST http://<IP>:8123/api/services/light/turn_on`
  Headers: `Authorization: Bearer <token>`
  Body: `{"entity_id": "light.living_room"}`
