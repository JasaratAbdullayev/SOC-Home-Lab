# Evidence and Accuracy Policy

This repository intentionally avoids screenshots and uses text-based documentation.

## Evidence labels

Use one of these labels in notes:

- **VERIFIED:** personally observed in the actual lab; include date, command/query, and sanitized output.
- **SYNTHETIC:** generated example data used to practice analysis.
- **ILLUSTRATIVE:** an example of what a report, query, or output could look like.
- **NOT VALIDATED:** configuration or rule has not yet been tested in the current deployment.
- **HYPOTHESIS:** an explanation that still needs supporting evidence.

## Never do this
- Do not invent terminal output and label it verified.
- Do not state a detection fired unless the dashboard or logs confirm it.
- Do not pass synthetic events off as collected endpoint telemetry.
- Do not publish secrets or unredacted personal information.

## Text evidence template

```text
Evidence label: VERIFIED / SYNTHETIC / ILLUSTRATIVE / NOT VALIDATED / HYPOTHESIS
Date/time and timezone:
Host or agent (sanitized):
Command or dashboard query:
Observed result:
Interpretation:
Limitations:
```
