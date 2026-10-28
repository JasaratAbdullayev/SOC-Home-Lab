# Lab Architecture

## Purpose

Practice a basic SOC workflow with an Ubuntu-based Wazuh deployment and a Windows endpoint in VirtualBox.

## Logical flow

```text
[Windows 10 VM]
  |  Wazuh agent / Windows event channels / optional Sysmon
  v
[VirtualBox lab network]
  |
  v
[Ubuntu Server VM]
  |-- Wazuh manager
  |-- Indexer and dashboard (deployment-dependent)
  v
[Analyst]
  |-- Search events
  |-- Validate context
  |-- Triage alerts
  |-- Document findings
```

## Network notes

Use a lab network appropriate to the VirtualBox setup. Avoid exposing management interfaces to the public internet. Do not publish internal IP addresses or hostnames if they reveal private details.

## Data flow and trust boundaries

- The Windows endpoint generates event telemetry.
- The Wazuh agent forwards configured events to the Wazuh deployment.
- The manager evaluates supported events and rules.
- The analyst verifies an alert using surrounding event context and endpoint details.
- An alert is an investigation lead, not proof of malicious activity by itself.

## Deployment-dependent details

Wazuh installation layouts vary by version and deployment type. Confirm component names and configuration paths in the actual installation before changing them.
