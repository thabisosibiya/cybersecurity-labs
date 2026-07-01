Windows Logon Investigation

Objective

Investigate Windows authentication events using Event Viewer to identify successful logons, failed logons, and privileged account activity.

⸻

Lab Environment

Component	Details
Operating System	Windows 11
Platform	UTM Virtual Machine
Tool	Windows Event Viewer
Log Source	Windows Security Log

⸻

Tools Used

* Windows Event Viewer
* Windows Security Logs

⸻

Investigation Steps

1. Opened Windows Event Viewer.
2. Navigated to Windows Logs → Security.
3. Filtered events using Event IDs 4624, 4625, and 4672.
4. Investigated successful logon activity.
5. Generated failed logon events by intentionally entering an incorrect password.
6. Reviewed privileged logon events.
7. Recorded observations and documented findings.

⸻

Evidence

Security Log Overview

Event ID 4624 – Successful Logons

Event ID 4624 – Event Details

Event ID 4625 – Failed Logons

Event ID 4625 – Event Details

Event ID 4672 – Privileged Logons

Event ID 4672 – Event Details

⸻

Analysis

Event ID 4624

Successful authentication events were reviewed to identify user logon activity and establish a baseline of normal system usage.

Event ID 4625

Failed authentication events were analysed to determine why logon attempts failed. These events are useful for identifying password guessing, brute-force attempts, or user authentication issues.

Event ID 4672

Privileged logon events were reviewed to identify accounts that received elevated privileges after successful authentication.

⸻

Key Findings

* Successfully filtered Windows Security logs using Event IDs.
* Identified successful and failed authentication events.
* Generated and analysed failed logon events in a controlled lab environment.
* Investigated privileged account logons.
* Practised documenting evidence in a structured investigation.

⸻

Skills Demonstrated

* Windows Event Viewer
* Windows Security Log Analysis
* Authentication Investigation
* Security Event Analysis
* SOC Alert Triage
* Technical Documentation

⸻

MITRE ATT&CK Mapping

Technique	ID
Valid Accounts	T1078
Brute Force	T1110

⸻

Conclusion

This lab provided practical experience investigating Windows authentication events and reinforced core SOC analyst skills, including log analysis, authentication monitoring, evidence collection, and security documentation.
