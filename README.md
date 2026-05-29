# Active Directory Home Lab

## Project Overview

This project demonstrates the deployment of a Windows Server 2022 Active Directory environment using Oracle VirtualBox.

The lab includes:

- Windows Server 2022 Domain Controller (DC01)
- Active Directory Domain Services (AD DS)
- DNS Configuration
- Organizational Units (OUs)
- Domain User Management
- Windows 10 Client Workstation
- Domain Join Operations
- User Authentication Testing

---

## Lab Architecture

Domain Name:
company.local

Domain Controller:
DC01

IP Address:
192.168.10.10

Client Workstation:
CLIENT01

IP Address:
192.168.10.20

---

## Objectives

- Deploy a Windows Server 2022 Domain Controller
- Install Active Directory Domain Services
- Configure DNS
- Create Organizational Units
- Create Domain Users
- Join Windows 10 Workstations to the Domain
- Test Domain Authentication
- Practice Active Directory Administration

---

## Tasks Completed

### Domain Controller Setup

- Installed Windows Server 2022
- Renamed server to DC01
- Configured static IP address
- Installed AD DS role
- Installed DNS role
- Promoted server to Domain Controller
- Created company.local forest

### Active Directory Administration

Created Organizational Units:

- IT
- Departments
- Workstations

Created test user account:

- rcrossan

### Windows 10 Client Setup

- Installed Windows 10
- Assigned static IP address
- Configured DNS to point to DC01
- Joined company.local domain
- Logged in using domain credentials

---

## Skills Demonstrated

- Active Directory Administration
- Windows Server 2022
- DNS Administration
- User Account Management
- Organizational Unit Management
- Domain Controller Deployment
- Windows 10 Administration
- Troubleshooting
- Virtualization using Oracle VirtualBox

---

## Future Enhancements

- Group Policy Management
- Password Policies
- Account Lockout Policies
- DHCP Configuration
- File Shares
- Security Groups
- PowerShell Automation
