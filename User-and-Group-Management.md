Windows User and Group Management

Objective

The objective of this exercise was to gain experience managing local users and groups within a Windows environment while applying the principle of least privilege.

This exercise focused on creating user accounts, reviewing administrative privileges, and using both graphical administration tools and command-line utilities to examine account information.

---

Accessing Local Users and Groups

Windows administrative tools were used to access local accounts and group information.

Navigation path:

```text
Computer Management
└── Local Users and Groups
    ├── Users
    └── Groups
```

This utility provides administrators with the ability to create, modify, disable, and manage local accounts and their permissions.


<img width="1016" height="781" alt="win9" src="https://github.com/user-attachments/assets/e97955ed-8618-4a02-9e6c-642ce9c6d0b2" />

Creating a Standard User Account

A standard user account named **analyst** was created to simulate the separation of administrative and non-administrative privileges.

The following settings were configured:

- Username: analyst
- User must change password at next logon: Disabled
- Password never expires: Enabled

Creating dedicated accounts is considered a security best practice because it limits unnecessary administrative access and improves accountability.

<img width="1013" height="773" alt="win10" src="https://github.com/user-attachments/assets/5f5aab4e-b167-4486-9833-7e2b49b644af" />


Reviewing Administrative Privileges

The local Administrators group was reviewed to identify accounts with elevated privileges.

This process demonstrates how security administrators verify permissions and apply the principle of least privilege.

<img width="1016" height="768" alt="win11" src="https://github.com/user-attachments/assets/072924d0-6688-4d4e-b103-377c994c7fc7" />




Command-Line User Enumeration

Windows command-line tools were used to gather information about local users and administrative groups.

Commands executed:

```cmd
whoami

net user

net localgroup administrators
```

These commands provide administrators with a fast and efficient method for auditing user accounts and permissions.

<img width="1011" height="631" alt="win12" src="https://github.com/user-attachments/assets/b4fa8168-5673-4245-9677-7c314ad8d358" />


# Why User Management Matters

User account management is one of the fundamental responsibilities of system administrators and security professionals.

Improperly configured accounts can increase the attack surface of a system and create opportunities for privilege escalation.

Effective user management helps organizations:

- Enforce the principle of least privilege
- Improve accountability
- Reduce unauthorized access
- Strengthen overall system security
- Simplify auditing and compliance efforts

---

# Analysis

This exercise provided practical experience with Windows account administration through both graphical tools and command-line interfaces.

The process reinforced the importance of separating administrative privileges from standard user privileges and demonstrated how administrators can verify permissions using built-in Windows utilities.

---

# Skills Demonstrated

- Windows Administration
- User Account Management
- Group Management
- Principle of Least Privilege
- Command Prompt (CMD)
- Access Control
- Security Administration
- Windows Security
- System Administration
- Technical Documentation
