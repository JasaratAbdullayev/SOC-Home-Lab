# SOC Investigation Methodology

Use this workflow for every investigation.

## 1. Validate the alert
- Record the alert timestamp and timezone.
- Record the rule ID, severity, description, agent, and source event.
- Confirm whether the alert is based on actual telemetry or a synthetic example.
- Check whether the event is complete and parseable.

## 2. Establish context
- What account and host are involved?
- Is the activity expected for that host and user?
- What happened immediately before and after the event?
- Are there related process, authentication, network, or system events?
- Is the system time correct?

## 3. Assess risk
Consider:
- asset importance,
- account privilege,
- evidence of repetition,
- unusual parent process or command line,
- unexpected network destinations,
- corroborating alerts,
- business context and false-positive possibilities.

## 4. Triage decision
Choose one and explain why:
- **Benign / expected:** supported by context; monitor if appropriate.
- **Suspicious / needs more evidence:** preserve evidence and investigate further.
- **Likely malicious:** multiple corroborating indicators support escalation.
- **Inconclusive:** insufficient telemetry or context.

Do not label activity malicious solely because it is unusual.

## 5. Document
Include:
- Summary
- Scope and time window
- Evidence and source
- Timeline
- Analysis and alternative explanations
- Severity and confidence
- Decision and rationale
- Recommended next steps
- Limitations

## 6. Response principles
Follow organizational authorization and procedures. In a home lab, practice with reversible actions. Do not isolate, disable, or delete production assets without authorization.
