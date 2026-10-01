# BlazingSystems Project Catalog

This catalog summarizes the public BlazingSystems portfolio and its validation status.

## Repository Model

| Repository | Purpose |
|---|---|
| [BlazingSystems-Projects](https://github.com/BlazingSystems/BlazingSystems-Projects) | Portfolio-ready demonstrations and usable builds |
| [BlazingSystems-Labs](https://github.com/BlazingSystems/BlazingSystems-Labs) | Active development requiring additional validation |
| [BlazingSystems-Experiments](https://github.com/BlazingSystems/BlazingSystems-Experiments) | Feasibility studies, compatibility work and prototypes |
| [BlazingSystems-Archives](https://github.com/BlazingSystems/BlazingSystems-Archives) | Sanitized historical notes, superseded concepts and recovery plans |

## Validation Levels

**Working build** — usable in its intended demonstration environment.  
**Source-ready** — coherent source is available; target hardware/platform validation remains.  
**Lab** — active implementation with specific unresolved validation tasks.  
**Experiment** — technical feasibility or compatibility study; not represented as a finished product.  
**Archive** — historical engineering notes only.

---

## Projects

### Marine Operations Logbook
**Area:** Offline web application  
**Status:** Demonstration build  
**Repository:** `BlazingSystems-Projects/marine/vessel-logbook/`

Generic offline operations logbook demonstrating local job setup, progress tracking, event timelines, lightweight calculation support and browser-local persistence. Public examples use fictional data only.

### Draft Reading Trainer
**Area:** Browser training application  
**Status:** Working build  
**Repository:** `BlazingSystems-Projects/marine/draftsight-trainer/`

Interactive visual-reading exercise for simulated vessel draft marks. The public edition is generic and independent of any company form or proprietary training system.

### Daily Operations Update
**Area:** Offline reporting tool  
**Status:** Demonstration build  
**Repository:** `BlazingSystems-Projects/marine/vessel-daily-updates/`

Single-page reporting demonstration for previous, current, to-date and balance figures using synthetic records.

### BlazeSystems Arcade
**Area:** Browser interface / game study  
**Status:** Demonstration build  
**Repository:** `BlazingSystems-Projects/games/blazesystems-arcade/`

Portable browser arcade/launcher study. The public edition uses an original mini-game and excludes commercial ROMs, BIOS files, copied game assets and third-party emulator payloads.

### Last Stand
**Area:** HTML5 game  
**Status:** Working build  
**Repository:** `BlazingSystems-Projects/games/last-stand/`

Dependency-free endless defense/strategy game designed for direct browser execution.

### ESP8266 Thermostat
**Area:** Embedded systems  
**Status:** Source-ready; hardware validation required  
**Repository:** `BlazingSystems-Projects/embedded/esp8266-thermostat/`

Standalone ESP8266 thermostat with DS18B20 sensing, relay output, local web interface, hysteresis control, anti-short-cycle timing and persistent settings.

### Captive Portal UI Demo
**Area:** Networking UI  
**Status:** Demonstration build  
**Repository:** `BlazingSystems-Projects/networking/captive-portal-ui-demo/`

Generic captive-portal interface study with plan selection, voucher input and session controls. The public demo is detached from production hotspot endpoints.

---

## Labs

### Blaze Pisonet Universal
ESP8266 timer/coin-control architecture with standalone and multi-unit concepts. Promotion requires exact-board compile, GPIO verification, persistence testing, failure recovery and multi-device validation.

### Blaze Pisonet Timer — Public-Safe Recovery
**Area:** ESP8266 timer / relay control  
**Status:** Lab / recovered derivative  
**Repository:** `BlazingSystems-Labs/embedded/blaze-pisonet-timer-public/`

Publication-safe derivative reconstructed from a recovered private timer branch. The public source removes the embedded MP3 payload and replaces the historical reusable AP password with a `CHANGE_ME` placeholder while preserving the core coin-input, dual-relay, TM1637 display, local web configuration, persistence, sales-counter, and warning workflow. The original recovered source/audio remain outside public GitHub. Exact-board compile and hardware validation remain.

### BlazeFM
Lightweight Android file-manager project with duplicate and image-similarity tooling. Remaining work includes full Gradle/device validation, modern storage-permission regression testing and signed release packaging.

### MachDownload
Segmented HTTP/HTTPS downloader. Python syntax and local range-download integrity tests pass; wider Windows/CDN/proxy/authentication validation remains.

### Local AI Studio
Local HTTP-based image/utility engine with optional model adapters. Core server validation is separate from model/runtime performance validation.

### OpenWrt VLAN Deployment Study
Sanitized networking study covering VLAN and management design. Raw device backups, private keys and deployment credentials are intentionally excluded.

### ESPHole
**Area:** ESP8266 networking / DNS filtering  
**Status:** Lab / source-ready  
**Repository:** `BlazingSystems-Labs/networking/esphole/`

Independent ESP8266 DNS-sinkhole and NAPT-repeater study. The public edition generates and persists unique first-boot AP/admin credentials. Exact-board compile, DNS/NAPT behavior and multi-client hardware validation remain.

### BlazeTube ESP8266
**Area:** ESP8266 networking / shared browser sessions  
**Status:** Lab / source-ready  
**Repository:** `BlazingSystems-Labs/networking/blazetube-esp8266/`

Shared browser-session coordinator and NAPT-repeater experiment using a user-supplied YouTube Data API key and official embedded playback in client browsers. No API credential is bundled. Compile, service-integration and hardware validation remain.

---

## Experiments

### BlazeAPK
**Current public build:** Beta 0.6

Browser-based APK/DEX parsing and Android-API compatibility research. The runnable public artifact is Beta 0.6; recovered Beta 0.7 material is design/implementation planning only and is not represented as a completed release. It is not presented as a replacement for Android Runtime/ART.

### BlazeJ2ME
**Current public build:** v1.6 universal compatibility fix

Single-file Java ME/JAR/JAD runtime experiment for compatibility research. The v1.6 artifact is the newest runnable build recovered so far; its JavaScript passes parser validation and it bundles no commercial JAR/JAD content.

### TokenLauncher
Android + ESP32 local token/device-control prototype. Security assumptions and unresolved kiosk/device-owner requirements are documented in the project.

### ESP8266 AP LED / Relay Controllers
Standalone access-point control experiments exploring lightweight embedded web interfaces.

### ESP8266 Arcade — Public-Safe Shell
**Area:** ESP8266 captive portal / networking  
**Status:** Experiment / recovered-design derivative  
**Repository:** `BlazingSystems-Experiments/embedded/esp8266-arcade-public/`

Publication-safe reconstruction of a recovered ESP8266 arcade architecture. The public source keeps captive DNS, a local web interface, generated AP credentials and optional NAPT support, but replaces the recovered emulator/ROM workflow with an original dependency-free mini-game. The raw recovered firmware remains outside public GitHub because its embedded portal included third-party runtime references and ROM-library behavior.

---

## Archived Engineering Topics

Sanitized historical notes and completion plans cover earlier work such as:

- five-sided ESP32 LED cube;
- ESP32 I2S noise-threshold controller;
- ESP8266 relay music sequencer;
- multi-node weather/flood monitoring thesis;
- MaSiCA machine-fault analyzer concept;
- OpenWrtFi architecture;
- Huawei HG8145v5 firmware/OpenWrt research;
- ESP8266 TOTP/2FA project;
- Dell Wyse 5070 homelab;
- older Pisonet/controller branches;
- motorcycle ESP32/LVGL HUD concept.

The public archive intentionally does **not** store raw employer/customer-era files, credentials, private network backups, proprietary forms, or confidential datasets.

## Publication Standard

Public project pages should contain:

1. purpose and scope;
2. current validation status;
3. requirements or target environment;
4. known limitations;
5. public-safe sample data;
6. preview/demo entry point where practical;
7. no confidential records, credentials or proprietary operational templates.

The portfolio is maintained as a technical engineering record rather than a raw development backup.
