# Changelog

## v0.3.0 — Starlink Telemetry

### Added
- Starlink telemetry from the existing read-only Peplink WAN API.
- MQTT Discovery sensors for firmware, hardware, uptime, boot count, antenna alignment, obstruction, download/upload bandwidth and POP latency.
- Per-sensor MQTT availability so Starlink metrics become unavailable when the dish is powered off or data is absent.
- Regression tests for online/offline Starlink and unrelated WANs.

### Notes
- No new API credentials, Starlink integration or router configuration changes required.
- Existing cellular, WAN, SIM and SpeedFusion processing is retained.
- Sensor units and live readings still require validation against InControl2.
- Starlink values are available only while the Peplink API supplies them.
