# Windows Home Lab Telemetry Portfolio

> A visual, documentation-first blue-team lab portfolio built around Windows host visibility, VM networking, telemetry preparation, and controlled security testing in an isolated environment.

![Lab connectivity](images/10-windows-to-kali-ping-success.png)

## Overview

This repository documents the build-out of a small Windows-focused cybersecurity lab created for defensive learning. The emphasis is on:

- validating downloaded software before installation
- designing an isolated VM network
- preparing Windows host logging for investigation
- documenting setup issues and troubleshooting
- generating observable host activity in a controlled lab
- capturing evidence in a format suitable for analyst-style reporting

## Lab Stack

- **Hypervisor:** Oracle VirtualBox
- **Attacker / test VM:** Kali Linux
- **Target VM:** Windows 10
- **Primary host visibility:** Windows Event Viewer
- **Additional tooling explored:** Splunk Enterprise, Sysmon
- **Rollback method:** VirtualBox snapshots

## Key Skills Demonstrated

- SHA256 integrity verification
- VM provisioning and segmentation
- static IP configuration
- Windows-to-Kali network validation
- troubleshooting telemetry tooling
- security logging preparation
- controlled host-based observation
- evidence capture and documentation

## Repository Layout

```text
.
├── images/
├── docs/
└── case-studies/
    ├── case-01-lab-build-and-telemetry-prep/
    └── case-02-controlled-simulation-and-host-observations/
```

## Featured Screens

### Software validation before install
![Checksum verification](images/03-powershell-sha256-verification.png)

### Static addressing for reliable lab communication
![Kali static IP](images/08-kali-ifconfig-static-ip.png)

### Connectivity validation from Windows to Kali
![Ping success](images/10-windows-to-kali-ping-success.png)

### Telemetry tool troubleshooting
![Splunk startup](images/14-splunk-webserver-startup-waiting.png)

### Controlled local file delivery inside the lab
![Lab HTTP server](images/17-local-http-server-running.png)

## Why this repo matters

A lot of beginner labs only show the final result. This one shows the full engineering process:

1. verify tools before installation
2. build isolated virtual infrastructure
3. validate addressing and connectivity
4. attempt richer telemetry tooling
5. fall back to native Windows visibility where appropriate
6. document lessons learned at each stage

That workflow reflects real analyst and engineer habits: build, validate, observe, troubleshoot, improve.

## Scope and Safety

All activity documented here was performed inside personally controlled virtual machines for educational, defensive, and research purposes. No production systems or third-party targets were involved.

This repository intentionally focuses on **lab setup, telemetry preparation, observable outcomes, and defensive analysis value**, rather than publishing offensive tradecraft as step-by-step instructions.

## Suggested reading order

1. [`docs/lab-overview.md`](docs/lab-overview.md)
2. [`docs/network-design.md`](docs/network-design.md)
3. [`docs/tooling-setup.md`](docs/tooling-setup.md)
4. [`docs/event-viewer-prep.md`](docs/event-viewer-prep.md)
5. [`case-studies/case-01-lab-build-and-telemetry-prep/README.md`](case-studies/case-01-lab-build-and-telemetry-prep/README.md)
6. [`case-studies/case-02-controlled-simulation-and-host-observations/README.md`](case-studies/case-02-controlled-simulation-and-host-observations/README.md)

## Future expansion

Planned follow-on cases for this lab:

- suspicious PowerShell execution review in Event Viewer
- process creation tracking with Event ID 4688
- scheduled task or persistence detection
- account change investigation
- comparison of native Windows logging vs richer endpoint telemetry

## Author note

This portfolio is designed to show not only technical ability, but also documentation quality, troubleshooting discipline, and blue-team thinking.
