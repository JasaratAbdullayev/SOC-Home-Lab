# Incident Report — IR-EXAMPLE-001

**Evidence label:** SYNTHETIC / ILLUSTRATIVE  
**Incident status:** Training scenario only; not a confirmed real incident.  
**Severity:** Undetermined without real telemetry.  
**Confidence:** Low, because this report uses synthetic data.

## Executive summary
An example review considers repeated Windows failed-logon events for a lab account. The scenario demonstrates triage documentation, not a verified detection.

## Scope
- Asset: `LAB-WIN10-EXAMPLE` (fictional)
- Account: `lab_user_example` (fictional)
- Source: `192.0.XX.XX` (documentation/example address)
- Time window: example timestamps only

## Timeline
- 09:XX:22 UTC — synthetic Event ID 4625 example.
- Additional events — not provided; no claims are made about further activity.

## Analysis
A failed-logon event indicates an unsuccessful authentication attempt. It does not by itself establish brute force, account compromise, or malicious intent. The analyst would look for repetition, account distribution, source consistency, successful logons, and expected operational context.

## Triage decision
**Suspicious / needs more evidence** is used only as an example training decision.

## Recommended actions
1. Confirm the event from real endpoint telemetry.
2. Search adjacent events and identify any successful logon.
3. Validate the source and account with the system owner.
4. If repeated unauthorized attempts are corroborated, follow the organization's account-protection and escalation process.
5. Preserve relevant logs and document timestamps/timezone.

## Limitations
- Synthetic event data only.
- No real alert or compromise is claimed.
- No rule firing is claimed.
- No containment or remediation was performed.
