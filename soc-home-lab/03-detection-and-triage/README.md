# 03 — Detection and Triage

This folder contains an example detection concept and an illustrative investigation. The rule has **not been validated** against the current Wazuh installation.

## Workflow
1. Identify the source event and its fields.
2. Confirm the source event is being collected.
3. Decide whether the detection is useful and sufficiently specific.
4. Test with benign and controlled lab events.
5. Inspect the resulting alert and false positives.
6. Record the rule version, test case, observed result, and limitations.

Do not paste custom XML into production. Back up configuration and validate syntax against the Wazuh version and official documentation first.
