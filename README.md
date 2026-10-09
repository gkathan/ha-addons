# GK Home Assistant Add-ons

A personal Home Assistant add-on repository for multiple projects.

## Add-ons

- **Peplink API Adapter** — read-only Peplink API to MQTT Discovery bridge. Current add-on version: `v0.1.0`.

## Adding the repository

In Home Assistant, open **Settings → Add-ons → Add-on Store → ⋮ → Repositories**, and add:

```text
https://github.com/gkathan/ha-addons
```

## Peplink notes

The adapter application and its container image are maintained in a separate private repository. The GHCR image is **private** and requires preconfigured Supervisor registry authentication with `read:packages`. No credentials belong in this public repository.

Supported image architectures: `aarch64` and `amd64`.

**Existing local Peplink add-on installations are not automatically migrated.** Register the repository first and plan migration carefully. Preserve the existing MQTT `device_id` and avoid running two adapter instances with the same discovery identity simultaneously.
