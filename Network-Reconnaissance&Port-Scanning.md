Objective

Perform a basic TCP port scan using Nmap to identify open ports on the Ubuntu virtual machine. Analyze the scan results and use service detection to identify the software associated with discovered ports.


Background

After identifying a live host through host discovery, the next step in network reconnaissance is determining which services are exposed.

Every network service communicates through one or more ports. By identifying open ports, security professionals can determine what applications are running and begin assessing the system's potential attack surface.

Nmap's default scan attempts to identify the most common TCP ports and determine whether they are open, closed, or filtered.


Part 1 – Performing a Basic Port Scan

The following command was executed:

nmap 127.0.0.1


The scan targeted the local Ubuntu system through the loopback interface.

Results indicated:

- 999 closed TCP ports
- 1 open TCP port

The only detected service was:

| Port | State | Service |
|631/tcp|Open|IPP (Internet Printing Protocol)|

<img width="1156" height="700" alt="nmap66" src="https://github.com/user-attachments/assets/953e7153-a41c-4c17-874b-60965ac25623" />




 Understanding the Results

Nmap reported:


Not shown: 999 closed tcp ports (conn-refused)


This indicates that the remaining scanned ports were reachable but were not accepting incoming connections.

The open port (631) is used by CUPS (Common Unix Printing System), Ubuntu's printing service.

Because this service is actively listening, Nmap classified the port as **Open**.

---

 Part 2 – Service Enumeration

After identifying the open port, service detection was performed.

Command executed:


nmap -sV 127.0.0.1


The **-sV** option attempts to determine which application is running on each discovered port.

The scan identified:

| Port | Service | Version |
|------|----------|---------|
|631/tcp|IPP|CUPS 2.4|

<img width="860" height="181" alt="nmap7" src="https://github.com/user-attachments/assets/12e31eb8-374b-4f77-8475-89c006771bc8" />


nmap -sV 127.0.0.1

 Why Service Enumeration Matters

Simply knowing that a port is open provides limited information.

Identifying the service and software version allows security professionals to:

- Determine what application is running
- Verify expected services
- Identify outdated software
- Prepare for vulnerability assessments
- Investigate potential attack vectors

Service enumeration is one of the most important steps before performing vulnerability scanning or penetration testing.



Analysis

The port scan successfully identified an open TCP service running on the Ubuntu virtual machine.

Service detection revealed that the open port was associated with the Common Unix Printing System (CUPS), version 2.4.

Although only one service was identified during this exercise, the workflow demonstrates how Nmap is used to discover exposed services and gather information that supports future security assessments.



Lessons Learned

- Performed a basic TCP port scan using Nmap.
- Identified an active network service.
- Distinguished between open and closed TCP ports.
- Used service version detection to identify running software.
- Developed an understanding of how exposed services contribute to a system's attack surface.

---

Skills Demonstrated

- Network Reconnaissance
- TCP Port Scanning
- Service Enumeration
- Nmap
- Linux Command Line
- Network Service Identification
- Cybersecurity Documentation



Key Takeaways

Port scanning is a fundamental reconnaissance technique used to identify exposed services on a target system. Combining port scanning with service version detection allows security professionals to better understand the target environment before conducting vulnerability assessments or penetration testing.

The information gathered during this exercise will be used in subsequent modules to explore operating system detection and compare reconnaissance techniques with Nessus vulnerability scanning.
