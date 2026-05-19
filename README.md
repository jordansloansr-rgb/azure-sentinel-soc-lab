# Azure Sentinel SOC Lab

## Overview
Built a cloud-based SOC lab in Microsoft Azure using Microsoft Sentinel, Log Analytics Workspace, and a Windows 10 virtual machine to collect and analyze Windows security events.

## Tools Used
- Microsoft Azure
- Microsoft Sentinel
- Log Analytics Workspace
- Windows 10 Virtual Machine
- Azure Monitor Agent (AMA)
- Kusto Query Language (KQL)
- Remote Desktop Protocol (RDP)

## What I Built
- Created an Azure resource group
- Deployed a Windows 10 VM in Azure
- Connected Windows Security Events to Microsoft Sentinel
- Configured AMA data connector
- Generated failed login attempts
- Queried security logs using KQL
- Investigated Event IDs 4624 and 4625

## Event IDs
- 4624 = Successful login
- 4625 = Failed login attempt

## Sample KQL Queries

### Failed Login Attempts
```kql
SecurityEvent
| where EventID == 4625
```

### Successful Logins
```kql
SecurityEvent
| where EventID == 4624
```

### Filtered Failed Logins
```kql
SecurityEvent
| where EventID == 4625
| project TimeGenerated, Account, Computer
```

## Skills Demonstrated
- SIEM monitoring
- Log analysis
- Threat investigation
- Windows event monitoring
- KQL querying
- Cloud security operations
- Azure administration

## Screenshots
See the screenshots folder for lab setup and query results.
