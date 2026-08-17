Windows Defender and Firewall

Objective

The objective of this exercise was to examine the built-in security controls available in Windows 11, with a focus on Microsoft Defender Antivirus and Windows Defender Firewall.

These technologies provide endpoint protection by detecting malicious software, monitoring security activity, and controlling network traffic entering and leaving the system.


Windows Security

Windows Security was opened to review the primary security controls protecting the Windows endpoint.

The Windows Security interface provides access to several security components, including:

- Virus & threat protection
- Firewall & network protection
- App & browser control
- Device security
- Account protection

Reviewing these controls provides an overview of the security posture of the Windows system.



<img width="1039" height="717" alt="ws1" src="https://github.com/user-attachments/assets/495c4297-aad9-49c7-b37e-50bb6c140208" />


Microsoft Defender Antivirus

The Virus & threat protection section was examined to review the antivirus protections enabled on the system.

Microsoft Defender Antivirus provides real-time protection against malware and other potentially unwanted threats. The interface also provides access to security updates, scanning options, and protection history.

Real-time protection was verified as enabled.

No security protections were disabled during this exercise.


<img width="1021" height="705" alt="ws2" src="https://github.com/user-attachments/assets/edcb2f60-fbed-495a-beec-ffea7357e7ff" />


Windows Firewall

The Firewall & network protection section was examined to review the firewall profiles configured on the system.

Windows Firewall uses different network profiles depending on the type of network connection:

- Domain network
- Private network
- Public network

Each profile can have different firewall policies and rules depending on the security requirements of the environment.

The active firewall profile was reviewed to verify that Windows Firewall was enabled.


<img width="1022" height="710" alt="ws3" src="https://github.com/user-attachments/assets/1016760f-33fa-46a1-94fb-b6c8b3871bd2" />


Advanced Firewall Rules

Windows Defender Firewall with Advanced Security was opened to examine the rules controlling network traffic.

The firewall uses separate rule sets for:

- Inbound traffic
- Outbound traffic

Inbound rules determine whether network connections attempting to reach the system are permitted or blocked.

Outbound rules determine whether applications and services are permitted to establish connections from the system to other hosts.

The existing inbound rules were reviewed without making unnecessary changes to the system configuration.

<img width="1314" height="989" alt="ws4" src="https://github.com/user-attachments/assets/4a701588-e779-4da6-93e0-38660b2a776d" />


Security Control Analysis

Microsoft Defender Antivirus and Windows Firewall provide two important layers of endpoint protection.

Defender Antivirus focuses primarily on identifying and preventing malicious software, while the firewall controls network communication based on configured rules and network profiles.

Together, these controls help reduce the attack surface of a Windows endpoint.

A simplified security model is:

```text
                    Windows Endpoint
                           │
              ┌────────────┴────────────┐
              │                         │
      Microsoft Defender        Windows Firewall
              │                         │
       Malware Detection          Network Control
              │                         │
              └────────────┬────────────┘
                           │
                    Endpoint Protection
```

 Why These Controls Matter

Endpoint security controls are particularly important in enterprise environments because individual workstations and servers can become targets for malware, unauthorized access, and network-based attacks.

Security professionals must understand how these controls operate in order to:

- Reduce attack surfaces
- Prevent malware infections
- Control unauthorized network connections
- Investigate security events
- Maintain secure endpoint configurations

These concepts also relate directly to vulnerability management and security monitoring activities performed elsewhere in this lab.



Analysis

This exercise provided hands-on experience reviewing the built-in security controls available in Windows 11.

Microsoft Defender and Windows Firewall were examined from both the standard Windows Security interface and the advanced firewall management interface.

The exercise demonstrated how endpoint protection involves multiple layers rather than relying on a single security mechanism.

The Windows security configuration will provide a foundation for the next phase of the lab, where the Windows endpoint will be evaluated using Nessus.

---

Skills Demonstrated

- Windows Security
- Microsoft Defender Antivirus
- Windows Firewall
- Firewall Rule Management
- Endpoint Security
- Network Access Control
- Security Configuration
- Windows Administration
- Security Monitoring Fundamentals
- Technical Documentation
