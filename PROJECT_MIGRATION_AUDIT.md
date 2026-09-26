# BlazingSystems Project Migration Audit

**Audit date:** 2026-09-26  
**Owner:** BlazingSystems  
**Purpose:** Recover, reconcile, validate, classify, and safely migrate projects created across ChatGPT sessions.

## Rules used for this migration

- Prefer the newest **actual recoverable artifact**, not whichever filename merely says `FINAL`.
- Preserve older versions when they add recovery/history value.
- Never replace a newer working artifact with an older one.
- Do not reconstruct missing source merely to populate GitHub.
- Separate unrelated projects even when they use the same technology.
- Distinguish **static/source validation** from **compiled/hardware validation**.
- Do not publish credentials, private financial/family/health/account material, employer-confidential material, copyrighted ROMs, or uninspected router backups.
- Third-party code keeps its upstream license and notices.

## Planned repository destinations

- **BlazingSystems-Projects** — working/usable releases
- **BlazingSystems-Labs** — active or source-only builds needing further validation
- **BlazingSystems-Experiments** — prototypes and technical proof-of-concepts
- **BlazingSystems-Archive** — superseded, incomplete, failed, or historical builds

> These repositories still need to exist before project source can be migrated into the agreed structure. The current GitHub integration can write repository content but does not expose repository creation.

## Recovered and reconciled projects

| Project | Canonical recovered artifact / lineage | Status | Audit result / next action |
|---|---|---|---|
| Last Stand HTML5 Game | `Last_Stand_HTML5_Game.zip` / single `index.html` | WORKING → Projects | Dependency-free single HTML. Inline JavaScript syntax check passed. Browser play-test still recommended for release notes. |
| DraftSight Trainer | `DST_DraftSight_Trainer_V5_Final_Audited.html` | WORKING / stable baseline → Projects | V5 is newer than V2/V3/V4 lineage. Inline JavaScript syntax check passed. Older versions retained only as history if useful. |
| Friv / Offline Arcade | `Friv_Offline_Arcade_MULTIEMU.html` plus older SNES builds | LICENSE REVIEW → Labs | All inline JS blocks pass syntax validation. No ROMs should be published. Emulator components have upstream licensing requirements; release needs preserved notices and must respect core-specific restrictions. |
| MachDownload | `MachDownload_v0.1_source_buildkit.zip` | WORKING SOURCE → Labs | Python compilation passed. Local HTTP Range self-test passed with final SHA-256 verification. No Windows EXE build/install validation in this environment. Generated `__pycache__` should be removed from public source. |
| Loumer Local AI Studio | `Loumer_Local_AI_Studio_v1.0_ENGINE.zip` | WORKING ENGINE / MODELS REQUIRED → Labs | Python source compiles. Local server starts and `/api/status` responds. Stable Diffusion/model generation not end-to-end tested because model weights are intentionally not bundled. |
| BlazeFM | `BlazeFM-source.zip` | SOURCE-ONLY → Labs | Real Android Studio source tree recovered; package `com.blazefm.blazesystems`, min API 21. No Gradle wrapper or compiled APK is present. Android SDK/build/install testing remains required. Similar-photo comparison is currently quadratic and should be optimized before very large libraries on low-memory phones. |
| Blaze Pisonet Universal | `BLAZE_PISONET_UNIVERSAL_FINAL.ino` | SOURCE-ONLY → Labs | Newest Pisonet lineage found. Source includes Standalone/Master/Slave roles, AP/STA modes, UDP coordination, ready/insert-coin display behavior, session accounting, and fallback AP. ESP8266 compile/hardware test still required. Older GPIO14/BOOTFIX/audio versions remain history. |
| ESP8266 Thermostat | recovered V1 + audited `ESP8266_Thermostat_FAILSAFE_V2.ino` | SOURCE-ONLY → Labs | Recovered V1 delayed sensor-fault OFF through the normal minimum-ON timer. V2 changes only fault shutdown so the relay de-energizes immediately. Target compilation, sensor-disconnect test, and relay test remain required. |
| LPB Neon Aero Portal | `LPB_Neon_Aero_Portal_v1.2_MULTICOINSLOT_FIX.zip` | SOURCE-ONLY / INTEGRATION TEST NEEDED → Labs | Inline JS syntax check passed. v1.2 repairs the multi-coinslot template structure. Final status still depends on a live LPB backend/template integration test. |
| Token Launcher | recovered prototype + audited v0.2 corrections | EXPERIMENTAL → Experiments | Found two concrete prototype issues: Android local HTTP needed explicit cleartext permission; ESP32 `/admin/test` dispensed test credit without the admin password. v0.2 source corrects both. Android/ESP32 compilation and device-owner/kiosk tests remain required. |
| ESP8266 AP LED Controller | `esp8266_ap_led_controller_fixed_v2.ino` | SOURCE-ONLY → Labs | Later source contains the `PWMRANGE` fallback intended to resolve the prior compile failure. No post-fix ESP8266 compile result was recoverable, so it is not marked verified. |
| Vessel LogBook / Draft Survey suite | V10/V10.4 deployment lineage | PRIVATE / PUBLIC-SANITIZATION REQUIRED | JavaScript syntax checks pass on recovered V8/V9/V10. Deployment builds contain corporate branding/form metadata; they are quarantined from public GitHub. A genuinely generic public edition should be produced separately rather than exposing branded deployment files. |
| Vessel TODATE Offline Web Archive | `Vessel_TODATE_Logbook_Offline_Web_Archive.html` | HISTORICAL WORKING → Archive | Recoverable single-HTML historical branch; superseded by later LogBook lineage. |
| Vessel Daily Updates Standalone | `Vessel_Daily_Updates_Standalone_FINAL.html` | HISTORICAL / ANCILLARY | Recovered as a separate helper. Keep separate from the main Vessel LogBook project and decide release status after sanitization review. |
| Ruijie/OpenWrt restore packages | several restore/backup `.tar.gz` files | PRIVATE QUARANTINE | Raw bytes could not be authorized for inspection in this audit workspace. Router backups can contain Wi-Fi keys, root hashes, MACs, or deployment identifiers, so they will not be published blindly. |
| Token/easy-wifi APK artifact | `easywifi.apk` | QUARANTINE | Binary exists without enough verified source/provenance context for public redistribution. |
| Debt dashboard/calendar artifacts | multiple HTML/ICS files | EXCLUDED | Personal financial material. Never publish to a public project repository by default. |

## Source not presently recoverable as a complete artifact

The following historical ideas/projects are known from prior work but no complete source artifact was recovered in the current Library sweep. They should **not** be recreated from memory merely to make GitHub look complete:

- OpenWrtFi full platform / three target firmware builds
- Huawei HG8145v5 OpenWrt flashing toolkit
- ESP32 LED Cube application framework
- ESP32 noise-threshold penalty controller
- ESP8266 TOTP appliance
- ESP8266 relay music sequencer
- distributed weather-node thesis firmware
- MaSiCA machine-fault analyzer
- Wyse 5070 homelab/PisoWiFi/SFTP deployment automation

For these, the resolution is to recover original source if it exists, or restart them later as clearly new implementations with the old design requirements documented.

## Validation levels

**WORKING** means a meaningful executable/source-level check passed and the recovered build is internally coherent.  
**SOURCE-ONLY** means source was recovered and statically audited, but the required target compiler/hardware/runtime is unavailable.  
**EXPERIMENTAL** means a prototype exists but important integration or deployment behavior still needs validation.  
**PRIVATE QUARANTINE** means the artifact is intentionally not being published until secrets/ownership/confidentiality are resolved.

## Immediate migration order once destination repositories exist

1. Last Stand HTML5 Game
2. DraftSight Trainer V5
3. MachDownload v0.1
4. Loumer Local AI Studio v1.0
5. BlazeFM
6. Blaze Pisonet Universal + useful history
7. ESP8266 Thermostat fail-safe V2 + recovered V1 history
8. LPB Neon Aero Portal v1.2
9. Token Launcher v0.2
10. ESP8266 AP LED Controller fixed_v2
11. Friv/Offline Arcade after third-party license notices are finalized
12. Historical archives
13. Private/quarantined networking and corporate deployment artifacts only after a separate sanitization/private-repository decision

---

**BlazingSystems migration principle:** preserve what actually exists, document what was actually tested, and never turn an unverified filename into a fake “final release.”
