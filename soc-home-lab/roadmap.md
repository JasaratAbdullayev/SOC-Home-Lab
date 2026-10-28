# Project Roadmap

This roadmap distinguishes planned work from verified work.

## Stage 1 — Wazuh SIEM baseline
- [ ] Confirm Wazuh manager service state on Ubuntu.
- [ ] Confirm the Windows agent appears in the agent list.
- [ ] Confirm recent Windows events appear in the dashboard.
- [ ] Record exact versions and deployment method.
- [ ] Document verified commands and sanitized outputs.

## Stage 2 — Windows event collection
- [ ] Review Security and System event collection.
- [ ] Confirm relevant event channels are enabled and collected.
- [ ] Generate benign test activity in the lab.
- [ ] Preserve only sanitized, authorized sample output.

## Stage 3 — Sysmon telemetry
- [ ] Install Sysmon from Microsoft's official Sysinternals distribution.
- [ ] Choose a reputable, maintained Sysmon configuration and review it before use.
- [ ] Configure Wazuh to collect the intended Sysmon channel.
- [ ] Verify actual Sysmon events arrive; record evidence in text, not screenshots.

## Stage 4 — Detection and triage
- [ ] Create or adapt a detection rule.
- [ ] Validate the rule against known benign and synthetic examples.
- [ ] Record false-positive considerations and required context.
- [ ] Map relevant behavior to MITRE ATT&CK only when the mapping is justified.

## Stage 5 — Incident response documentation
- [ ] Document scope, timeline, evidence, confidence, and limitations.
- [ ] Separate confirmed observations from hypotheses.
- [ ] Recommend proportionate containment and recovery actions.

## Stage 6 — Future extensions
- [ ] Network monitoring and firewall logs.
- [ ] Identity and access monitoring.
- [ ] Additional Windows telemetry and response playbooks.
- [ ] Integrate components only after each individual stage is understood.

**Not included at this stage:** phishing project, screenshots, or claims of unverified successful tests.
