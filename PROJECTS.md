# BlazingSystems Project Index

This is the audited public recovery and migration ledger for BlazingSystems projects.

Status is based on the latest **actual recovered artifact and verified GitHub state**. A file is not treated as production-ready merely because its filename contains words such as `final`.

## Repository Map

- **Projects** — verified usable/canonical builds  
  https://github.com/BlazingSystems/BlazingSystems-Projects

- **Labs** — active development and source-ready work still requiring validation  
  https://github.com/BlazingSystems/BlazingSystems-Labs

- **Experiments** — prototypes, compatibility work, reverse engineering and exploratory builds  
  https://github.com/BlazingSystems/BlazingSystems-Experiments

- **Archives** — superseded, incomplete, failed, historical and unrecovered-project resolution records  
  https://github.com/BlazingSystems/BlazingSystems-Archives

---

## Projects — Canonical / Usable

### Vessel LogBook

**Status:** FINAL / USABLE  
**Location:** `BlazingSystems-Projects/marine/vessel-logbook/`  
**Canonical recovered build:** V10.4 Audio + Haptic Final

The V10.4 branch supersedes the earlier V8/V9/V10/V10.1–V10.3 branches as the public canonical build. Older meaningful milestones are preserved in Archives.

### DraftSight Trainer

**Status:** FINAL / AUDITED  
**Location:** `BlazingSystems-Projects/marine/draftsight-trainer/`  
**Canonical recovered build:** V5 Final Audited

Older V2/V3/V4 milestones are preserved in Archives.

### Vessel Daily Updates

**Status:** USABLE  
**Location:** `BlazingSystems-Projects/marine/vessel-daily-updates/`

Standalone lightweight daily-update tool recovered and published separately from the larger Vessel LogBook.

### BlazeSystems Arcade

**Status:** USABLE / PORTABLE HYBRID  
**Location:** `BlazingSystems-Projects/games/blazesystems-arcade/`

The Portable Hybrid build is the current canonical branch. Selected Friv/SNES/MULTIEMU milestones are preserved in Archives.

### Last Stand

**Status:** USABLE HTML5 BUILD  
**Location:** `BlazingSystems-Projects/games/last-stand/`

Lightweight browser strategy/endless-mode game recovered as an actual runnable HTML5 build.

### ESP8266 Thermostat

**Status:** SOURCE READY / HARDWARE VALIDATION REQUIRED  
**Location:** `BlazingSystems-Projects/embedded/esp8266-thermostat/`

Complete standalone AP thermostat source with persistent settings, DS18B20 support, relay control, hysteresis and anti-short-cycle logic. Exact board/wiring validation remains deployment-specific.

### LPB Neon Aero Portal

**Status:** WORKING SOURCE / TARGET-INTEGRATION REQUIRED  
**Location:** `BlazingSystems-Projects/networking/lpb-neon-aero-portal/`

Latest recovered v1.2 multi-coinslot branch. Live behavior still depends on the target LPB PisoWiFi server endpoints and captive-browser environment.

---

## Labs — Active / Source-Ready

### Blaze Pisonet Universal

**Status:** ACTIVE / SOURCE-ONLY  
**Location:** `BlazingSystems-Labs/embedded/blaze-pisonet-universal/`

Latest recovered Pisonet firmware branch. It supersedes the older Embedded Audio / GPIO14 / boot-fix generations as the active codebase.

Still required before promotion:
- exact-board compile
- hardware GPIO verification
- relay fail-safe testing
- coin-noise/bounce testing
- persistence/power-loss testing
- AP/STA validation
- long-duration timer-drift test
- real multi-unit/master-slave validation

### BlazeFM

**Status:** ACTIVE / SOURCE TREE RECOVERED  
**Location:** `BlazingSystems-Labs/android/blazefm/`

Recovered Android/Gradle project includes MainActivity, FileEngine, BlazeProvider, manifest, resources and build files. The source tree has been reconstructed from the real recovered package rather than from memory.

Still required:
- Android Studio/Gradle build validation
- modern storage-permission testing
- duplicate-finder stress testing
- lint/crash audit
- signed release packaging

### MachDownload

**Status:** WORKING ALPHA / SOURCE TREE  
**Location:** `BlazingSystems-Labs/software/machdownload/`

Recovered segmented HTTP/HTTPS downloader project with local build scripts. Broader protocol/auth/proxy/browser-integration and resilient-resume testing remain future work.

### Loumer Local AI Studio

**Status:** ENGINE / LAB  
**Location:** `BlazingSystems-Labs/ai/local-ai-studio/`

Recovered local-AI engine/web UI work for low-resource machines. Model/runtime compatibility remains external to the core project.

### Ruijie EW1200G OpenWrt VLAN Deployment

**Status:** DEPLOYMENT LAB / SANITIZED RECORD  
**Location:** `BlazingSystems-Labs/networking/ruijie-ew1200g-openwrt/`

Raw OpenWrt backup archives are intentionally **not public** because recovered backups contain device-specific credentials and private host/server keys. The public repository contains the sanitized deployment record and resolution path instead.

---

## Experiments

### BlazeAPK

**Status:** EXPERIMENTAL / BETA  
**Location:** `BlazingSystems-Experiments/web/blazeapk/`

Canonical active build is Beta 0.5. Alpha 0.1–0.3 milestones are preserved in Archives. Not presented as a general Android runtime replacement.

### BlazeJ2ME

**Status:** EXPERIMENTAL / BETA  
**Location:** `BlazingSystems-Experiments/web/blazej2me/`

Offline single-file Java ME/JAR/JAD emulation experiment. Compatibility varies by application/runtime.

### TokenLauncher

**Status:** SECURITY / DEVICE-CONTROL PROTOTYPE  
**Location:** `BlazingSystems-Experiments/android/token-launcher/`

Recovered Android + ESP32 prototype with subsequent security/integration patches and a documented resolution.

### ESP8266 AP LED Controller

**Status:** PROTOTYPE / SOURCE  
**Location:** `BlazingSystems-Experiments/embedded/esp8266-ap-led-controller/`

### ESP8266 Relay Controller

**Status:** PROTOTYPE / SOURCE  
**Location:** `BlazingSystems-Experiments/embedded/esp8266-relay-controller/`

---

## Archives — Preserved History

### Vessel LogBook History

Selected V8, V9, V10 and V10.3 milestones are preserved under:

`BlazingSystems-Archives/marine/vessel-logbook-history/`

### DraftSight Trainer History

Selected V2/V3/V4 milestones are preserved under:

`BlazingSystems-Archives/marine/draftsight-trainer-history/`

### Blaze Pisonet Timer History

Embedded Audio V2, GPIO14 Final, GPIO14 Bootfix and audit documentation are preserved under:

`BlazingSystems-Archives/embedded/blaze-pisonet-timer-history/`

### BlazeAPK / BlazeJ2ME Alpha History

Superseded browser-runtime milestones are preserved under:

`BlazingSystems-Archives/web-runtime-history/`

### Friv / Arcade History

Selected early fixed, SNES-playable and MULTIEMU milestones are preserved under:

`BlazingSystems-Archives/games/friv-arcade-history/`

---

## Unrecovered / Resolution-Only Projects

The following projects have meaningful historical design or partial-work records but no trustworthy final source artifact was recovered from the available Library. They are documented with recovery/completion resolutions rather than fabricated replacement code:

- ESP32 / WS2812 five-sided LED Cube
- ESP32 I2S noise-threshold penalty controller
- ESP8266 relay music sequencer
- multi-node weather/flood thesis system
- MaSiCA machine-fault analyzer
- OpenWrtFi
- Huawei HG8145v5 OpenWrt reverse-engineering/recovery
- ESP8266 TOTP / 2FA project
- Dell Wyse 5070 homelab work
- ESP8266 remote LAN access/tunnel gateway
- older coin-operated water-vending controller
- older Arduino Mega centralized Pisonet controller
- motorcycle ESP32/LVGL HUD concept

Resolution records live in:

`BlazingSystems-Archives/resolutions/`

If an original file is later recovered, it should be preserved unchanged in Archives first, audited, then resumed from a cleaned copy in Labs.

---

## Intentionally Excluded From Public GitHub

The migration does **not** publish:

- debt dashboards or debt-recovery calendars
- private financial/account information
- personal health/family material
- credentials/tokens/passwords
- private router/host keys
- raw OpenWrt backups containing secrets
- employer-confidential operational records
- unrelated personal media

---

## Migration / Audit Rules

1. Recover real artifacts before documenting releases.
2. Never replace a newer working build with an older file just because the older filename sounds more final.
3. Preserve meaningful prior versions as history.
4. Keep unrelated projects isolated.
5. Do not reconstruct missing historical source and present it as original.
6. Source-only embedded firmware must not be labeled production-ready without compile/hardware validation.
7. Experimental reverse-engineering work must be labeled clearly.
8. Every active project should have a README with status, purpose, requirements, limitations and validation notes.
9. Public archives must be sanitized for secrets and private data.
10. Failed or superseded work is preserved when it has engineering value instead of being silently erased.

The migration is intentionally conservative: **recoverability, provenance and accuracy matter more than repository count.**
