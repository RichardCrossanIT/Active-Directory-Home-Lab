# Active Directory Home Lab

## Project Overview

This project documents the deployment of a small Active Directory lab environment using Oracle VirtualBox, Windows Server 2022, and Windows 10.

The purpose of this lab is to practice core IT support and system administration tasks including Windows Server setup, Active Directory Domain Services, DNS configuration, domain user management, and workstation domain joining.

---

## Lab Environment

| System   | Role                           | Operating System    | IP Address    |
| -------- | ------------------------------ | ------------------- | ------------- |
| DC01     | Domain Controller / DNS Server | Windows Server 2022 | 192.168.10.10 |
| CLIENT01 | Domain-Joined Workstation      | Windows 10 Pro      | 192.168.10.20 |

Domain Name:

```text
company.local
```

---

## Network Architecture

```text
DC01 - Windows Server 2022
IP Address: 192.168.10.10
Roles:
- Active Directory Domain Services
- DNS Server

        |
        |
        v

CLIENT01 - Windows 10 Pro
IP Address: 192.168.10.20
DNS Server: 192.168.10.10
Domain: company.local
```

---

## Objectives

* Create a Windows Server 2022 virtual machine
* Configure a static IP address
* Install Active Directory Domain Services
* Promote the server to a Domain Controller
* Create a new Active Directory forest and domain
* Configure DNS for domain name resolution
* Create Organizational Units
* Create domain user accounts
* Install and configure a Windows 10 client workstation
* Join the workstation to the domain
* Verify domain authentication using Active Directory credentials

---

## Deployment Steps

### 1. Created the Domain Controller VM

Created a new virtual machine in Oracle VirtualBox named:

```text
DC01
```

Installed Windows Server 2022 and configured the VM with assigned CPU, memory, storage, and internal networking.

---

### 2. Configured Static IP Address

Configured DC01 with a static IP address so the domain controller and DNS server would have a consistent network address.

DC01 network configuration:

```text
IP Address: 192.168.10.10
Subnet Mask: 255.255.255.0
Preferred DNS Server: 192.168.10.10
```

---

### 3. Installed Active Directory Domain Services

Using Server Manager, installed the following roles:

* Active Directory Domain Services
* DNS Server

These roles allow the server to manage domain users, computers, authentication, and name resolution.

---

### 4. Promoted Server to Domain Controller

Promoted DC01 to a Domain Controller and created a new forest:

```text
company.local
```

During promotion, DNS and Global Catalog options were enabled.

---

### 5. Verified Active Directory and DNS

Confirmed that the domain was created successfully and that DNS was resolving the domain name.

Verified domain name resolution from CLIENT01 using:

```cmd
ping company.local
```

The domain resolved to:

```text
192.168.10.10
```

---

### 6. Created Organizational Units

Created custom Organizational Units in Active Directory to organize users and computers.

Created OUs:

```text
IT
Departments
Workstations
```

These OUs simulate a basic business structure for managing users, computers, and future Group Policy settings.

---

### 7. Created Domain User Account

Created a domain user account in Active Directory:

```text
rcrossan
```

This account was used to test domain authentication from the Windows 10 client workstation.

---

### 8. Created Windows 10 Client VM

Created a second virtual machine named:

```text
CLIENT01
```

Installed Windows 10 Pro and connected it to the same internal VirtualBox network as DC01.

---

### 9. Configured Client Network Settings

Configured CLIENT01 with a static IP address and pointed DNS to DC01.

CLIENT01 network configuration:

```text
IP Address: 192.168.10.20
Subnet Mask: 255.255.255.0
Preferred DNS Server: 192.168.10.10
```

This allowed CLIENT01 to locate the domain controller through DNS.

---

### 10. Joined CLIENT01 to the Domain

Joined CLIENT01 to the Active Directory domain:

```text
company.local
```

Successfully received the confirmation message:

```text
Welcome to the company.local domain.
```

---

### 11. Verified Domain Login

Successfully logged into CLIENT01 using the domain account:

```text
company\rcrossan
```

This confirmed that Active Directory authentication was working properly.

---

## Tasks Completed

* Installed Windows Server 2022
* Configured DC01 with a static IP address
* Installed Active Directory Domain Services
* Installed DNS Server role
* Promoted DC01 to a Domain Controller
* Created the company.local domain
* Created Organizational Units
* Created a domain user account
* Installed Windows 10 Pro on CLIENT01
* Configured CLIENT01 network settings
* Verified DNS resolution
* Joined CLIENT01 to the domain
* Verified domain authentication with company\rcrossan

---

## Skills Demonstrated

* Windows Server 2022 Administration
* Active Directory Domain Services
* Domain Controller Deployment
* DNS Configuration
* Active Directory Users and Computers
* Organizational Unit Management
* User Account Creation
* Windows 10 Administration
* Domain Join Operations
* Domain Authentication
* Basic Network Configuration
* Troubleshooting DNS and Connectivity
* Oracle VirtualBox Virtualization

---

## Project Outcomes

Successfully deployed a functioning Active Directory lab environment.

Verified:

* DC01 operating as a Domain Controller
* DNS resolving company.local
* CLIENT01 communicating with DC01
* CLIENT01 joined to the company.local domain
* Domain user account successfully logging into CLIENT01

---

## Screenshots

Screenshots will be added as the project progresses.

Planned screenshots include:

* Server Manager showing DC01 and company.local
* Active Directory Users and Computers
* Organizational Units
* Domain user account
* DNS verification using ping company.local
* CLIENT01 domain join confirmation
* Successful domain login using company\rcrossan

---

## Future Enhancements

Planned additions to this lab:

* Password reset practice
* Account lockout and unlock testing
* Security group creation
* Group Policy configuration
* Password policy enforcement
* DHCP server configuration
* Shared folder and NTFS permissions
* Remote Desktop administration
* PowerShell automation
* Basic security hardening

---

## Summary

This lab provided hands-on experience with core Windows enterprise administration concepts. By building a Domain Controller, configuring DNS, creating users and OUs, joining a Windows 10 workstation to the domain, and testing domain authentication, this project demonstrates foundational skills used in IT Support, Help Desk, Desktop Support, System Administration, and Cybersecurity roles.
