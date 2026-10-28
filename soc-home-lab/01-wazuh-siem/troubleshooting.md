# Wazuh Troubleshooting Notes

Troubleshoot from the simplest dependency outward.

1. **Windows service stopped:** inspect the service state and agent log on Windows.
2. **Agent absent from manager list:** verify agent enrollment and configuration.
3. **Agent disconnected:** check network reachability, manager address, ports, and time synchronization.
4. **Agent active but no expected events:** verify Windows event channels and Wazuh collection configuration.
5. **Events exist but no alert appears:** an event may be collected without matching an alert rule. Review archives/alerts and rule logic appropriate to the deployment.

Useful initial commands:

Ubuntu:
```bash
sudo systemctl status wazuh-manager
sudo /var/ossec/bin/agent_control -l
sudo tail -n 100 /var/ossec/logs/ossec.log
```

Windows PowerShell:
```powershell
Get-Service -Name Wazuh
Get-WinEvent -LogName Security -MaxEvents 10
```

These commands are diagnostic steps, not proof of a successful result. Save the real output if you need to claim a check passed.
