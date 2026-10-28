# Sysmon Setup and Validation

## Download and safety
Obtain Sysmon from Microsoft's official Sysinternals distribution. Review Microsoft's documentation and the configuration you choose. Do not run unknown scripts or blindly apply an untrusted configuration.

## Install
The exact command depends on the downloaded filename and chosen configuration. From an elevated terminal in the folder containing Sysmon, a typical pattern is:

```powershell
.\Sysmon64.exe -accepteula -i .\sysmonconfig.xml
```

Use this only if the executable and configuration files actually have those names. A maintained community configuration can be useful, but review its source and settings first.

## Validate
```powershell
Get-Service -Name Sysmon64 -ErrorAction SilentlyContinue
Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" -MaxEvents 10
```

The service name can vary. Verify the actual installed service and event channel.

## Wazuh collection
Wazuh must be configured to collect the Sysmon Operational channel. The exact configuration location and syntax depend on the agent version and existing configuration. Back up the configuration before editing, use the documented syntax for your version, and restart only the relevant service after reviewing the change.

## Evidence to record
- Sysmon version and source
- Configuration source and commit/version
- Whether installation was verified
- Whether events appear locally
- Whether events reach Wazuh
- Any missing event types or filtering limitations

**Status:** NOT VALIDATED until checked in the actual lab.
