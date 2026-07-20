Objective

Install Nmap on the Ubuntu virtual machine and verify that the installation was successful. Nmap serves as the primary network reconnaissance tool used throughout this module to discover hosts, identify open ports, enumerate services, and gather information prior to vulnerability assessment.



Part 1 – Verifying Installation Status

Before installing Nmap, the system was checked to determine whether the software was already available.

The following command was executed:

nmap --version


Ubuntu reported that the command was not installed and suggested installation methods.

<img width="966" height="582" alt="nmap1" src="https://github.com/user-attachments/assets/1ff68704-52e2-4793-ae4a-7a55bc49e61f" />



Part 2 – Installing Nmap

The package repository was updated before installing Nmap using Ubuntu's Advanced Package Tool (APT).

Commands executed:


sudo apt update
sudo apt install nmap


The installation completed successfully without errors.


<img width="983" height="647" alt="nmap2" src="https://github.com/user-attachments/assets/a10180a8-d1eb-491b-a867-526127397cd4" />


Part 3 – Verifying Installation

After installation, the following command was executed (nmap --version). The output confirmed that Nmap was installed successfully and displayed the installed version.

<img width="988" height="110" alt="nmap3" src="https://github.com/user-attachments/assets/f6399f52-66db-49fc-970f-476388bb5d91" />

 Identifying the Target System

Before performing network reconnaissance, the IP address of the Ubuntu virtual machine was identified.

The following command was executed:

hostname -I

The command returned the IPv4 address assigned to the virtual machine. Knowing the correct IP address is essential before beginning any network assessment, as Nmap requires a valid target host or network.
<img width="562" height="126" alt="nmap4" src="https://github.com/user-attachments/assets/ea8d546c-081d-47f1-99fe-a893012fb932" />

Host Discovery

The first reconnaissance scan performed with Nmap was a host discovery scan.

Command executed:

nmap -sn 10.0.2.15

The -sn option performs a ping scan that determines whether a host is online without performing a port scan.

This type of scan is commonly used at the beginning of security assessments to identify which systems are active before more detailed scanning begins.

Host Discovery Results

The scan successfully identified the Ubuntu virtual machine as an active host.

Nmap reported that the host was online and responded to network probes.

Although only a single host was scanned in this exercise, the same technique can be applied to an entire subnet to quickly identify live systems within an enterprise network.

<img width="562" height="126" alt="nmap4" src="https://github.com/user-attachments/assets/f5c04aa9-68b0-4a80-9c0e-9be7b4dab2a2" />

Why Host Discovery Matters

Host discovery is typically the first step in network reconnaissance.

Rather than immediately scanning every possible IP address, security professionals first determine which systems are active. This reduces scan time, minimizes unnecessary network traffic, and ensures that subsequent assessments focus only on reachable systems.

Examples include:

- Identifying newly deployed servers
- Building network inventories
- Preparing vulnerability assessments
- Validating asset management records
- Locating unauthorized or unknown devices

Analysis

Nmap was successfully installed and configured on the Ubuntu virtual machine. Initial reconnaissance began by identifying the assigned IPv4 address before performing a host discovery scan. The host discovery scan confirmed that the Ubuntu virtual machine was reachable across the network. Although only a single host was scanned during this exercise, the same technique is commonly used against entire network ranges to identify active devices prior to vulnerability assessments.
This exercise establishes the reconnaissance phase of the cybersecurity assessment process and prepares the environment for future port scanning, service enumeration, and operating system detection.


Lessons Learned

- Verified software availability before installation.
- Installed Nmap using Ubuntu's package manager.
- Confirmed the installation using version verification.
- Identified the IP address of the target system.
- Performed a successful host discovery scan.
- Learned how reconnaissance fits into the vulnerability assessment lifecycle.
- Prepared the environment for advanced Nmap scanning techniques.

Commands Used


nmap --version

sudo apt update

sudo apt install nmap

hostname -I

nmap -sn 10.0.2.15

Skills Demonstrated

- Ubuntu Linux
- Linux Command Line
- APT Package Management
- Network Reconnaissance
- Host Discovery
- IPv4 Address Identification
- Nmap
- Cybersecurity Documentation
