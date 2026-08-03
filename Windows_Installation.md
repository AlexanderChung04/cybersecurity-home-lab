Windows 11 Installation

Objective

The objective of this phase was to deploy a Windows 11 virtual machine within the cybersecurity home lab environment. This system will serve as the primary Windows endpoint for future activities involving system hardening, vulnerability management, network analysis, Active Directory, Sysmon, Windows Defender, and SIEM integration.

---

Virtual Machine Configuration

Oracle VirtualBox was used to create the virtual machine. A Windows 11 ISO image was attached to the virtual optical drive, and the following hardware resources were allocated.

| Setting | Value |
|----------|--------|
| Operating System | Windows 11 (64-bit) |
| Memory | 4096 MB |
| Processors | 2 |
| Storage | 64 GB |
| Firmware | UEFI |
| Network Mode | NAT |


<img width="635" height="381" alt="windows2" src="https://github.com/user-attachments/assets/f4b224c9-27e3-4901-af10-3286f3650b12" />
<img width="613" height="156" alt="windows1" src="https://github.com/user-attachments/assets/ded435d9-433b-43d5-9c0f-c9aa071308e1" />



Initial Boot Troubleshooting

During the initial installation attempt, the virtual machine displayed a black screen after startup. Investigation of the VirtualBox logs and system configuration confirmed that the ISO image had been mounted correctly and that UEFI initialization was functioning normally.

Further analysis revealed that the virtual machine required user input when the following prompt appeared:


Press any key to boot from CD or DVD...


Once a key was pressed, the installation process proceeded normally.

This troubleshooting process reinforced the importance of validating boot sequences, installation media, and virtualization settings before assuming an operating system failure.



Windows Installation

After booting successfully from the installation media, the Windows installation process was started.

The following options were selected:

- Language: English (United States)
- Keyboard layout: US
- Installation type: Custom installation
- Operating system: Windows 11 Pro
- Storage location: 64 GB virtual disk

---

<img width="1910" height="997" alt="wind7" src="https://github.com/user-attachments/assets/dc5db4bd-1a48-405a-909a-66e1ba779e8d" />


Initial System Configuration

After installation, the initial setup process was completed and the operating system booted successfully.

Additional security configuration and system administration tasks will be performed during subsequent phases of the project.

---<img width="1917" height="1018" alt="wind8" src="https://github.com/user-attachments/assets/a7793b49-901b-45f6-b320-4fab0f605e4f" />



# Analysis

The successful deployment of a Windows virtual machine expanded the cybersecurity home lab environment beyond Linux administration and vulnerability assessment. Establishing a dedicated Windows system provides the foundation for future work involving operating system hardening, event logging, vulnerability management, network monitoring, and enterprise administration.

The installation process also demonstrated the importance of methodical troubleshooting when working with virtualization technologies.

---

# Skills Demonstrated

- Oracle VirtualBox
- Windows 11 Administration
- Operating System Deployment
- UEFI Configuration
- Virtual Machine Management
- System Troubleshooting
- Log Analysis
- Virtual Networking
- Technical Documentation
