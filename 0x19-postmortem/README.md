## Outage Incident Report
## Issue Summary
- Duration:
Start Time: January 15, 2024, 09:30 AM EAT
End Time: January 15, 2024, 11:45 AM EAT
- Impact:
The user authentication service experienced a complete outage.
Users were unable to log in or access secured resources during the outage.
Approximately 30% of users were affected.
- Root Cause:
Database connection pool exhaustion due to misconfigured connection settings.
## Timeline
- Detection Time:
January 15, 2024, 09:30 AM EAT
- Detection Method:
An automated monitoring alert triggered due to a spike in failed authentication attempts.
- Actions Taken:
Initial investigation focused on the authentication service logs.
Assumed a potential DDoS attack due to the sudden increase in failed login attempts.
- Misleading Paths:
Invested time analyzing network traffic for signs of malicious activity.
Examined server logs for unusual patterns, leading to unnecessary diversion of resources.
- Escalation:
Escalated to the DevOps team to investigate server resource utilization.
Involved the Database Administration team to inspect database connection logs.
- Resolution:
Identified misconfigured database connection pool settings causing rapid exhaustion.
Adjusted connection pool parameters and restarted the authentication service.
## Root Cause and Resolution
- Root Cause:
Misconfigured database connection pool settings led to a rapid increase in open connections, exhausting available resources.
- Resolution:
Adjusted connection pool parameters to ensure more efficient utilization.
Implemented a rolling restart of affected services to apply configuration changes.
## Corrective and Preventative Measures
- Improvements/Fixes:
Implemented automated checks for connection pool settings during deployment.
Enhanced monitoring to proactively identify potential database connection issues.
- Tasks:
Added anomaly detection for abnormal spikes in authentication failures.
Conducted a thorough review of connection pool settings across the entire web stack.
Introduced automated testing for configuration changes related to critical services.
## Conclusion
The  outage on January 15, 2024, resulted from a misconfiguration in the database connection pool settings. This incident significantly impacted the user authentication service, rendering it temporarily unavailable. The swift response of the technical teams, combined with a focused investigation, led to the identification of the root cause and the implementation of corrective measures.
To prevent future occurrences, the team will conduct a comprehensive review of connection pool settings and introduce automated checks during deployment. Additionally, enhanced monitoring and anomaly detection will be implemented to provide early warnings of potential database connection issues. By addressing these specific tasks, we aim to fortify the resilience of our web stack and ensure a more reliable user experience moving forward.


