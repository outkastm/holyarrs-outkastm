# HolyArrs for TerraMaster TOS 7

HollyArrs is a self-hosted web dashboard and companion tool for managing and monitoring your `*arr` media automation stack (such as Sonarr, Radarr, Lidarr, Readarr, and Prowlarr), optimized for deployment on TerraMaster TOS 7 NAS systems.

## 1. Overview & Source Repository

* **Application Name:** HolyArrs
* **Container Image Source:** Pulled directly from official Docker Hub / GHCR repository (`holyarrs/holyarrs:version`)
* **Application Storage Path:** `/Volume*/DockerAppData/holyarrs-outkastm`
* **Upstream Source Repository:** <https://github.com/holyarrs/holyarrs>
* **Support:** <https://tmnascommunity.eu/forums/topic/holyarrs-docker>

## 2. Port & Network Configuration

* **Host Published Port:** `6262`
* **Internal Container Port:** `6262`
* **Protocol:** HTTP

Upon installation via the TOS App Center, the web interface is accessible at `http://<NAS_IP_ADDRESS>:6262`.

## 3. Persistent Data Directories

To ensure configuration files, `*arr` instance connections, and application settings persist across package updates and system reboots, host directories are mapped directly to NAS storage (`/Volumex`):

| Host Path | Container Target Path | Purpose |
| ----- | ----- | ----- |
| `/Volume*/DockerAppData/holyarrs-outkastm/config` | `/config` | Application configuration, API keys, and local settings |

## 4. Privacy Policy & Data Handling (Compliance Item 4)

This application strictly operates locally on your TerraMaster NAS and connects only to the self-hosted `*arr` services you explicitly configure.

* **Upstream Project & Source Repository:** <https://github.com/holyarrs/holyarrs>

### Privacy & Telemetry Statements:

1. **No External Tracking / Telemetry:** HollyArrs stores all data locally on your infrastructure and contains no external telemetry, tracking, or analytics. It does not transmit personal data, media library metadata, or usage metrics to external servers.
2. **Local Processing & Storage:** All instance URLs, API keys, and operational configurations remain exclusively on your local NAS device within `/Volume*/DockerAppData/holyarrs-outkastm/config`.

## 5. Installation & Deployment Guide

### Installation via TOS App Center

1. Open **TOS App Center** on your TerraMaster NAS.
2. Search for the **HollyArrs** app and install it.
3. Launch the application or navigate directly to `http://<NAS_IP>:6262`.

## 6. License

* **Upstream Application:** Governed under the upstream open-source license (<https://github.com/hollyarrs/hollyarrs/blob/main/LICENSE>).