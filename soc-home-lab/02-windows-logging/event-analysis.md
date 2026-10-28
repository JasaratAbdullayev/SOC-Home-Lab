# Windows Event Analysis Notes

## Authentication investigation
For a failed-logon event, examine:
- timestamp and timezone,
- target account,
- logon type,
- source workstation or network address when available,
- status/substatus,
- repetition and surrounding events,
- whether the user confirms expected activity.

## Process investigation
For process-creation telemetry, examine:
- image path and filename,
- command line,
- parent process,
- user and integrity context,
- process hash if collected,
- nearby network or authentication events,
- whether the action fits the host's role.

## Network investigation
For network telemetry, examine:
- initiating process,
- source and destination,
- destination port and protocol,
- expected business purpose,
- DNS/proxy/firewall context if available,
- frequency and timing.

## Analyst cautions
- A single event rarely proves malicious intent.
- Event collection depends on audit policy and configuration.
- Missing telemetry is not proof that an activity did not occur.
- Keep observed facts separate from interpretation.
