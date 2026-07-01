Windows Logon Investigation

Overview

This lab demonstrates how to investigate Windows authentication events using Windows Event Viewer. The objective was to identify successful logons, failed logons, and privileged account activity by analysing the Windows Security log.

Objectives

* Investigate successful authentication events (Event ID 4624)
* Investigate failed authentication events (Event ID 4625)
* Review privileged logon events (Event ID 4672)
* Understand how Windows records authentication activity
* Practice documenting findings as a SOC analyst

⸻

Lab Environment

* Windows 11 Virtual Machine
* Windows Event Viewer

⸻

Event IDs Investigated

Event ID	Description
4624	Successful Logon
4625	Failed Logon
4672	Special Privileges Assigned

⸻

Investigation Steps

1. Opened Event Viewer.
2. Navigated to Windows Logs → Security.
3. Filtered the Security log using Event IDs.
4. Reviewed successful logons (4624).
5. Generated failed logons by intentionally entering an incorrect password.
6. Reviewed privileged logons (4672).
7. Recorded observations and documented the investigation.

⸻

Investigation Evidence

Security Log Overview

Shows the Windows Security log before filtering.

⸻

Event ID 4624 – Successful Logons

Filtered the Security log to display successful authentication events.

⸻

Event ID 4624 – Event Details

Reviewed the event details including account name, logon type, and timestamp.

⸻

Event ID 4625 – Failed Logons

Generated failed authentication events by entering an incorrect password.

⸻

Event ID 4625 – Event Details

Reviewed the failure reason, status code, sub-status code, and logon type.

⸻

Event ID 4672 – Privileged Logons

Reviewed events showing accounts that received elevated privileges.

⸻

Event ID 4672 – Event Details

Analysed the privileges assigned after successful authentication.

⸻

Skills Demonstrated

* Windows Event Viewer
* Windows Security Log Analysis
* Authentication Investigation
* Security Event Filtering
* Basic SOC Alert Triage
* Security Documentation

⸻

Key Takeaways

This investigation demonstrates how Windows records authentication activity and how these logs can be analysed to identify successful logons, failed logons, and privileged account activity. These are fundamental investigation techniques used by SOC analysts during authentication-related security investigations.
