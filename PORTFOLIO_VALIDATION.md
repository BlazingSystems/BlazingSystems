# Portfolio Validation Record

This document summarizes the validation boundary of the public BlazingSystems portfolio.

Public repositories contain sanitized demonstrations, source-ready projects, experiments, and engineering notes. Validation claims below apply only to the public editions currently published.

## Projects

| Project | Public status | Validation |
|---|---|---|
| Marine Operations Logbook | Demonstration build | Browser-local workflow and synthetic-data demo; not an operational survey system |
| Draft Reading Trainer | Working browser build | Standalone browser exercise; generic training scale |
| Daily Operations Update | Demonstration build | Standalone browser reporting demo using synthetic records |
| BlazeSystems Arcade | Demonstration build | Original browser launcher/mini-game edition; commercial ROMs and third-party payloads excluded |
| Last Stand | Working browser build | Dependency-free HTML5 game; JavaScript syntax previously checked |
| ESP8266 Thermostat | Source-ready | Source is coherent; exact-board, sensor-disconnect, relay, and long-duration hardware validation remains |
| Captive Portal UI Demo | Demonstration build | Standalone interface study; no production hotspot backend is included |

## Labs

| Project | Public status | Remaining validation |
|---|---|---|
| Blaze Pisonet Universal | Lab / source-ready | ESP8266 compile, GPIO behavior, persistence, recovery, and multi-device hardware tests |
| Blaze Pisonet Timer | Lab / recovered derivative | Complete recovered source structure is published with a placeholder credential and empty audio arrays; ESP8266 compile, relay/coin/display behavior, persistence and hardware endurance tests remain |
| BlazeFM | Lab / source-ready | Gradle build, Android storage-permission regression tests, device validation, signed packaging |
| MachDownload | Lab / working alpha | Wider Windows, CDN, proxy, authentication, and release-build testing |
| Local AI Studio | Lab / engine prototype | Model-dependent generation and performance testing with user-supplied model weights |
| OpenWrt VLAN Deployment Study | Lab / documentation | Target-router deployment and rollback validation using sanitized configuration data |
| ESPHole | Lab / source-ready | Public credential hardening complete; ESP8266 compile, DNS/NAPT, recovery and multi-client hardware validation remain |
| BlazeTube ESP8266 | Lab / source-ready | No bundled API key; public credential hardening complete; ESP8266 compile, NAPT, API and multi-client validation remain |

## Experiments

BlazeAPK Beta 0.6, BlazeJ2ME v1.6, TokenLauncher, and the ESP8266 controller studies remain experimental. BlazeAPK 0.6 and BlazeJ2ME v1.6 pass JavaScript parser validation; broader runtime compatibility testing remains. None is represented as production-ready software.

## Publication Boundary

Public editions use generic interfaces, fictional or placeholder data, and no production credentials, raw router backups, private keys, employer/client records, commercial ROMs, or proprietary operational datasets.

Validation is intentionally separated into source/static checks, controlled functional tests, target-platform testing, and real hardware/deployment testing. A project is not promoted merely because it compiles or opens successfully.
