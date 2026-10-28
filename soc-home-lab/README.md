# SOC Home Lab — Wazuh, Windows Logging, Detection & Incident Triage

> **Project status:** documentation and example artifacts prepared for a home lab.  


## Objective

Build a small defensive-security lab that demonstrates a SOC L1 workflow:

1. Collect Windows endpoint telemetry with Wazuh.
2. Improve endpoint visibility with Sysmon.
3. Review and triage security events.
4. Map relevant behaviors to MITRE ATT&CK.
5. Write investigation notes and an incident report.
6. Keep reproducible technical documentation suitable for a GitHub portfolio.

## Lab concept

- **Ubuntu Server VM:** Wazuh manager/indexer/dashboard components, depending on the installed deployment.
- **Windows 10 VM:** Wazuh agent and Windows event sources.
- **Virtualization:** Oracle VirtualBox.
- **Analyst workflow:** collect → detect → validate context → triage → document → recommend response.

This is a conceptual layout. Adapt component names and addresses to the actual deployment.

## Repository guide

- `docs/` — architecture, setup notes, and investigation methodology.
- `01-wazuh-siem/` — service checks, agent checks, and validation checklist.
- `02-windows-logging/` — Windows event collection and Sysmon setup notes.
- `03-detection-and-triage/` — example detection logic, investigation notes, and an illustrative incident report.
- `samples/` — clearly labeled synthetic events for practicing analysis.
- `roadmap.md` — staged future improvements.


## Safety and privacy

- Use an isolated, authorized lab only.
- Do not run attack simulations against systems you do not own or have permission to test.
- Do not publish private IP details, usernames, tokens, API keys, real event data, or personal information.
- Synthetic sample logs are for documentation and analyst practice; they are not genuine telemetry.
- No screenshots are included. No phishing project is included.

## Suggested first validation pass

1. Confirm Wazuh services on Ubuntu.
2. Confirm the Windows agent is listed as active.
3. Confirm recent Windows events arrive in the dashboard.
4. Record the exact time range and the query used.
5. If no events arrive, troubleshoot collection before moving to detection engineering.

See `01-wazuh-siem/validation-checklist.md`.
