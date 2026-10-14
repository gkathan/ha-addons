# Peplink API Adapter

Read-only Peplink router telemetry for Home Assistant using MQTT Discovery.

## What it does
- Polls the local Peplink API and publishes WAN, cellular and SpeedFusion sensors.
- Optionally publishes SIM status sensors.
- From v0.3.0, publishes Starlink diagnostics when the WAN API exposes them.
- When Starlink is switched off, Starlink measurement sensors become unavailable instead of displaying stale readings.

## Requirements
- Peplink router with compatible firmware (validated on 8.6.1).
- Peplink API client with `api.read-only` scope.
- Reachable MQTT broker and unique device ID per installation.

## Operation
The adapter polls at the configured interval (30 seconds by default). No router write commands or Starlink controls are used.

## Updating
Updates are released through the HA add-on repository. Keep automatic updates disabled if you want to approve each installation manually.
