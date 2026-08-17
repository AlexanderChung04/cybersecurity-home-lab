Windows Event Viewer

Objective

The objective of this exercise was to gain experience using Windows Event Viewer to analyze system activity, security events, and operating system logs.

Event Viewer is one of the primary tools used by system administrators, incident responders, and security analysts to investigate suspicious behavior, review system activity, and monitor the health of Windows systems.

This exercise focused on examining Windows logs, identifying common event sources, and understanding how analysts use event data during investigations.

---

Accessing Event Viewer

Event Viewer was opened from the Windows administrative tools menu.

<img width="1016" height="781" alt="win9" src="https://github.com/user-attachments/assets/e6315038-bdd1-4b44-b987-383cab519101" />


Navigation path:

```text
Event Viewer
└── Windows Logs
    ├── Application
    ├── Security
    ├── Setup
    ├── System
    └── Forwarded Events
```

<img width="1023" height="780" alt="win12" src="https://github.com/user-attachments/assets/6f250277-09c3-4c98-9ac1-e857d7ca945d" />

These logs contain information about application activity, user authentication, system services, drivers, hardware, and security events.





Security Log Analysis

The Security log was examined to identify authentication activity and system events recorded by Windows Security Auditing.

Several Audit Success events were observed, indicating normal system activity.

Common events included:

- Successful logon events
- Privilege assignments
- Account activity
- Authentication events

Examples of frequently encountered event identifiers include:

| Event ID | Description |
|----------|-------------|
| 4624 | Successful logon |
| 4634 | User logoff |
| 4672 | Special privileges assigned |

---

<img width="1031" height="771" alt="win13" src="https://github.com/user-attachments/assets/15987436-fda7-41c5-a348-d427c2cf650f" />

Event Analysis

Individual events were examined in greater detail using the General and Details tabs.

These tabs provide additional information regarding:

- User accounts
- Event timestamps
- Security identifiers (SIDs)
- Process information
- Authentication details

This information allows security analysts to reconstruct activity timelines and investigate potentially malicious behavior.

---

<img width="1025" height="767" alt="win14" src="https://github.com/user-attachments/assets/b5bf0d8b-c6e6-4f38-9687-5875746045dc" />


System Log Analysis

The System log was reviewed to observe operating system activity related to drivers, services, startup processes, and kernel events.

Common sources included:

- Service Control Manager
- Kernel-General
- Kernel-Boot
- EventLog
- DistributedCOM

These events help administrators identify system failures, driver problems, service interruptions, and unexpected operating system behavior.

---

<img width="1022" height="756" alt="win15" src="https://github.com/user-attachments/assets/bbdba285-1d29-4df6-b80d-541ddce51411" />


Why Event Viewer Matters

Event logs are among the most valuable sources of information available during security investigations.

Security teams routinely analyze event logs to:

- Investigate unauthorized access attempts
- Identify suspicious user activity
- Detect privilege escalation
- Examine system failures
- Establish timelines during incident response

Understanding how to locate and interpret these logs is a fundamental cybersecurity skill.

---

Analysis

This exercise provided hands-on experience with one of the most important tools available within Windows environments.

Reviewing both Security and System logs reinforced the importance of centralized logging, event correlation, and continuous monitoring within enterprise environments.

This knowledge will serve as a foundation for future work involving Sysmon, Windows Defender, Wazuh, and incident response procedures.

---

Skills Demonstrated

- Windows Administration
- Event Viewer
- Log Analysis
- Windows Security Auditing
- Event Correlation
- Incident Response Fundamentals
- Security Monitoring
- System Administration
- Technical Documentation
