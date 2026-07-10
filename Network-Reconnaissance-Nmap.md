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

After installation, the following command was executed:


nmap --version


The output confirmed that Nmap was installed successfully and displayed the installed version.

### Screenshot 3

 Identifying the Target System

Before performing network reconnaissance, the IP address of the Ubuntu virtual machine was identified.

The following command was executed:

```bash
hostname -I
```

The command returned the IPv4 address assigned to the virtual machine.

Knowing the correct IP address is essential before beginning any network assessment, as Nmap requires a valid target host or network.

### Screenshot 4




hostname -I




 Host Discovery

The first reconnaissance scan performed with Nmap was a host discovery scan.

Command executed:


nmap -sn 10.0.2.15



The -sn option performs a ping scan that determines whether a host is online without performing a port scan.

This type of scan is commonly used at the beginning of security assessments to identify which systems are active before more detailed scanning begins.

### Screenshot 5

**Figure 5.** Running a host discovery scan against the Ubuntu virtual machine.

```
Insert Screenshot:
nmap -sn 10.0.2.X
```

---

# Host Discovery Results

The scan successfully identified the Ubuntu virtual machine as an active host.

Nmap reported that the host was online and responded to network probes.

Although only a single host was scanned in this exercise, the same technique can be applied to an entire subnet to quickly identify live systems within an enterprise network.

### Screenshot 6

**Figure 6.** Results of the Nmap host discovery scan.

```
Insert Screenshot:
Host is up
Scan completed
```

---

# Why Host Discovery Matters

Host discovery is typically the first step in network reconnaissance.

Rather than immediately scanning every possible IP address, security professionals first determine which systems are active. This reduces scan time, minimizes unnecessary network traffic, and ensures that subsequent assessments focus only on reachable systems.

Examples include:

- Identifying newly deployed servers
- Building network inventories
- Preparing vulnerability assessments
- Validating asset management records
- Locating unauthorized or unknown devices

# Analysis

Nmap was successfully installed using Ubuntu's default package manager. Installing the software through APT ensures that updates can be managed using the operating system's package management system.

Verifying the installation confirms that the environment is properly configured for future reconnaissance exercises.

---

# Lessons Learned

- Verified software availability before installation.
- Installed software using Ubuntu's APT package manager.
- Confirmed successful installation using version verification.
- Prepared the environment for network reconnaissance activities.

---

# Skills Demonstrated

- Ubuntu Linux
- APT Package Management
- Software Installation
- Command Line Interface (CLI)
- Nmap Installation
- Environment Preparation
- Linux System Administration
