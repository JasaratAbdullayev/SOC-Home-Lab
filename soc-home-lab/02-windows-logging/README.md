# 02 — Windows Logging

The objective is to understand the source events before writing detections.

## Event sources
- Windows Security log: authentication and security-related events, depending on audit policy.
- Windows System log: operating-system and service events.
- Sysmon Operational log: detailed process and network telemetry when Sysmon is installed and configured.

## Basic local check

PowerShell (run with suitable permissions):

```powershell
Get-WinEvent -LogName Security -MaxEvents 10 |
  Select-Object TimeCreated, Id, ProviderName, Message
```

For Sysmon, if installed:

```powershell
Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" -MaxEvents 10 |
  Select-Object TimeCreated, Id, ProviderName, Message
```

If a log channel does not exist or access is denied, document the actual error and check installation, permissions, and policy. Do not invent output.

## Example event IDs (context matters)
- 4624: successful logon
- 4625: failed logon
- 4688: process creation, when the relevant audit policy is enabled
- Sysmon Event ID 1: process creation
- Sysmon Event ID 3: network connection, when enabled in configuration

Event IDs need surrounding fields and context; they are not verdicts by themselves.
