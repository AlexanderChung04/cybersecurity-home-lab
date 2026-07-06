Built a home lab using VirtualBox, Ubuntu, Windows, and Nessus to gain hands-on cybersecurity experience.
-  Create Ubuntu VM
-  Create Windows VM
-  User accounts
-  Permissions
- Firewalls
- Nessus vulnerability scans
- Documentation and final report

Objective
Identify and remediate outdated software packages on the Ubuntu virtual machine.

## Tools Used
- Ubuntu APT Package Manager
- Nessus Essentials

## Commands Executed
bash
sudo apt update
apt list --upgradable
sudo apt upgrade
sudo reboot

## Findings
- Initial assessment identified 46 packages requiring updates.
- Security-related updates included Python, gzip, tar, and other core system packages.
- All updates were successfully installed.
- Validation confirmed the system had no remaining available package upgrades.

## Skills Demonstrated
- Linux package management
- Patch management
- Vulnerability remediation
- Validation of security updates 

