Objective

Use Nmap's operating system fingerprinting capabilities to identify the operating system running on the target machine and demonstrate how security professionals gather system information during the reconnaissance phase of an assessment.


Background

After identifying live hosts and open ports, attackers and security professionals attempt to determine which operating system is running on a target.

Knowing the operating system allows analysts to better understand the environment, identify likely services, and narrow the search for potential vulnerabilities.

Nmap performs operating system detection by sending specially crafted packets to the target and comparing the responses against its fingerprint database.


Part 1 – Operating System Detection

Operating system fingerprinting was performed using the following command:

sudo nmap -O 127.0.0.1

The **-O** option enables OS detection.

Because operating system fingerprinting requires raw packet generation, administrative privileges (`sudo`) were required.

Nmap identified the operating system as Linux with a confidence level of up to 97%.

Although an exact match was not found, the returned results closely matched several Linux kernel versions.

<img width="1220" height="252" alt="nmap8" src="https://github.com/user-attachments/assets/e73570ca-b07a-42a3-99fe-bf84932cec1b" />

sudo nmap -O 127.0.0.1



Understanding OS Fingerprinting

Unlike service detection, operating system detection does not examine installed software directly.

Instead, Nmap analyzes how the operating system responds to specially crafted network packets.

Characteristics such as:

- TCP sequence generation
- Window sizes
- ICMP responses
- TCP options
- Packet timing

are compared against Nmap's fingerprint database to estimate the operating system.

For this scan, Nmap determined the host was running Linux with a high confidence score.

Part 2 – Aggressive Scan

A more comprehensive reconnaissance scan was then performed.

Command executed:

sudo nmap -A 127.0.0.1


The **-A** option enables several advanced reconnaissance techniques simultaneously, including:

- Operating System Detection
- Service Version Detection
- Default Nmap Scripting Engine (NSE) scripts
- Traceroute

The scan successfully identified:

- CUPS version 2.4
- HTTP service information
- robots.txt information
- Operating system fingerprint
- Network distance

<img width="1211" height="327" alt="nmap9" src="https://github.com/user-attachments/assets/67a0cd0b-41b5-4a83-abbb-b1ccc1e2b3f8" />


sudo nmap -A 127.0.0.1


Understanding the Aggressive Scan

The aggressive scan expands upon earlier reconnaissance by combining multiple information gathering techniques into a single command.

Compared to previous scans, the output now included:

- Service version information
- HTTP server details
- HTTP title information
- robots.txt discovery
- Operating system fingerprinting
- Network distance

Rather than executing several separate scans, the aggressive scan provides a broad overview of the target system that can assist during vulnerability assessments or penetration testing.


Analysis

Nmap successfully identified the host as a Linux-based operating system with a confidence level of up to 97%.

Although an exact operating system fingerprint was not available, the returned results closely matched multiple Linux kernel versions, demonstrating how Nmap estimates operating systems using network behavior rather than directly querying the host.

The aggressive scan also identified additional information about the running CUPS service, including version details and HTTP metadata, illustrating how multiple reconnaissance techniques can be combined into a single assessment.


Lessons Learned

- Performed operating system fingerprinting using Nmap.
- Interpreted confidence-based OS detection results.
- Used the aggressive scan option (-A).
- Collected operating system and service information simultaneously.
- Learned how reconnaissance techniques build upon one another during security assessments.


Skills Demonstrated

- Nmap
- Operating System Fingerprinting
- Network Reconnaissance
- Service Enumeration
- Linux Command Line
- Information Gathering
- Security Documentation


Key Takeaways

Operating system detection is an important stage of network reconnaissance because it helps identify the technologies running on a target before vulnerability assessment begins.

The aggressive scan demonstrated how Nmap can combine several reconnaissance techniques into a single command, allowing analysts to efficiently collect operating system, service, and network information while reducing the number of individual scans required.
