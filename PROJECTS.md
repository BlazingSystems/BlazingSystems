# BlazingSystems Project Index

This is the public recovery and migration index for projects created, repaired, audited, or preserved through the BlazingSystems workflow.

> Status is based on the latest actual artifact recovered. A project is not marked FINAL merely because a filename says "final".

## Production / Usable

| Project | Latest recovered artifact | Status | Notes |
|---|---|---|---|
| Vessel LogBook | Vessel_LogBook_V10_4_AUDIO_HAPTIC_FINAL.html + V10.4 corporate package | FINAL / USABLE | Latest recovered branch includes audio/haptic feedback and SOF reminder work. Earlier V7–V10.3 builds are preserved as history, not canonical releases. |
| DraftSight Trainer | DST_DraftSight_Trainer_V5_Final_Audited.html | FINAL / AUDITED | Training simulator with configurable ready countdown, timed scoring, keyboard controls, persistent settings, and scenario flow. |
| BlazeSystems Arcade | BlazeSystems_Arcade_PORTABLE_HYBRID.html | USABLE / PORTABLE | Latest recovered hybrid build. Earlier Friv/SNES/MULTIEMU builds remain useful history. |
| LPB Neon Aero Portal | portal_v1_2.html / v1.2 multi-coinslot fix package | WORKING SOURCE | LPB PisoWiFi Lite portal rebuild with coin-slot integration. Live server behavior still depends on the target LPB installation. |
| ESP8266 Thermostat | ESP8266_Thermostat.ino | SOURCE READY | Standalone AP thermostat UI with relay control and persistent settings. Physical sensor/relay validation remains device-specific. |

## Active / Labs

| Project | Latest recovered artifact | Status | Resolution |
|---|---|---|---|
| Blaze Pisonet Universal | BLAZE_PISONET_UNIVERSAL_FINAL.ino | ACTIVE / SOURCE-ONLY | Newer than the earlier Embedded Audio and GPIO14 branches. Needs exact-board compile + hardware validation before being labeled production firmware. |
| BlazeFM | BlazeFM-source.zip | ACTIVE / SOURCE-ONLY | Android file manager architecture recovered. Still needs Gradle/build validation, Android storage testing, duplicate-finder stress tests, lint/crash audit, and signed release build. |
| MachDownload | MachDownload_v0.1_source_buildkit.zip | WORKING ALPHA | Segmented HTTP/HTTPS downloader build kit recovered. Core direct-download/resume path exists; browser interception, queues, auth, proxy, refreshed URLs, and adaptive segmentation remain future work. |
| Loumer Local AI Studio | Loumer_Local_AI_Studio_v1.0_ENGINE.zip | ENGINE / LAB | Local AI engine package recovered. Model acquisition/runtime compatibility remains external to the engine package. |
| BlazeAPK | BlazeAPK_Alpha_0.1.html + package | ALPHA / LAB | APK-in-browser/sandbox experiment. Treat as experimental compatibility work, not a general Android runtime replacement. |
| OpenWrt / Ruijie EW1200G configs | restore and backup tar.gz sets | DEPLOYMENT LAB | Several restore/config iterations recovered, including VLAN10, DHCP management, SSH/Telnet, and maintenance variants. Must remain hardware/model-specific. |

## Experiments

| Project | Artifact / evidence | Status | Notes |
|---|---|---|---|
| Last Stand HTML5 Game | Last_Stand_HTML5_Game.zip | PROTOTYPE | Small HTML5 strategy/endless-mode game build recovered. |
| ESP8266 AP LED / Relay Controllers | fixed_v2 and relay .ino files | PROTOTYPE / SOURCE | Standalone AP web-control experiments recovered. |
| Friv Offline Arcade lineage | multiple SNES, MULTIEMU, server, hybrid, portable builds | SUPERSEDED EXPERIMENTS | Kept as lineage leading to BlazeSystems Arcade. |
| OpenWrtFi | design/master build specification | UNIMPLEMENTED | Requirements exist for Ruijie EW1200G Pro, Orange Pi Zero 3, and x86/OpenWrt PC, but no verified deployable implementation has been recovered yet. |

## Archived / Unresolved Historical Work

These are preserved as engineering history rather than presented as finished builds:

- Older ESP8266 TOTP / DS1302 / OLED work — unresolved library/API conflicts in historical chats; no verified deployable artifact recovered.
- Older Arduino Mega centralized Pisonet controller — concept and debugging history exist, but no final validated artifact has been recovered.
- Superseded Vessel LogBook V7/V8/V9/V10.0–V10.3 branches.
- Superseded Blaze Pisonet Embedded Audio / GPIO14 / boot-fix branches once the Universal branch is validated.
- Failed/empty Friv output artifacts are not treated as releases.

## Migration Rules

1. Recover actual artifacts before documenting a release.
2. Never replace a newer working build with an older file because the older filename looks more "final."
3. Preserve useful prior versions as history.
4. Keep unrelated projects isolated.
5. Do not publish private financial, health, family, account, credential, or employer-confidential material.
6. Source-only embedded firmware must not be called production-ready until it compiles for the target board and is hardware-tested.
7. Experimental reverse-engineering work must be labeled clearly.
8. Each migrated project receives its own README, status, known limitations, build/use instructions, and audit notes.

## Intended Repository Layout

- **BlazingSystems-Projects** — verified usable releases
- **BlazingSystems-Labs** — active development and source-ready builds
- **BlazingSystems-Experiments** — prototypes, reverse engineering, and uncertain compatibility work
- **BlazingSystems-Archive** — superseded, failed, incomplete, or historical artifacts

The migration is intentionally conservative: recoverability and accuracy matter more than making the repository count look impressive.
