# 01 — Wazuh SIEM Baseline

Goal: verify service health, agent connectivity, and event ingestion before building detections.

## Ubuntu service check

Run on the Ubuntu Server VM:

```bash
sudo systemctl status wazuh-manager
```

If the deployment uses additional services, check them according to the installed Wazuh version and installation method.

## Agent list

```bash
sudo /var/ossec/bin/agent_control -l
```

Interpret the actual output rather than assuming the agent is connected. A listed agent may still be disconnected.

## Check manager logs

```bash
sudo tail -n 100 /var/ossec/logs/ossec.log
```

For live observation while troubleshooting:

```bash
sudo tail -f /var/ossec/logs/ossec.log
```

Stop live output with `Ctrl+C`.

## Windows service check

Run in an elevated PowerShell window on Windows:

```powershell
Get-Service -Name Wazuh
```

Service name and behavior may vary by installed agent version.

## Validation sequence

1. Confirm the manager is running.
2. Confirm the agent service is running on Windows.
3. Confirm the agent is listed and connected on Ubuntu.
4. Search the dashboard for recent events from that agent.
5. Record only the output actually observed.

See `validation-checklist.md`.
