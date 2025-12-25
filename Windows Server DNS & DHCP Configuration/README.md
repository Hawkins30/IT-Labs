# Lab — Windows Server DNS & DHCP Configuration

## Purpose

The purpose of this lab is to demonstrate the configuration and verification of DNS and DHCP services on Windows Server within an Active Directory domain environment. DNS and DHCP are foundational services required for domain functionality, client connectivity, and network management. This lab reflects common real-world IT support and junior system administration tasks.

---

## Tools Used

- Windows Server 2022
- DNS Manager
- DHCP Manager
- Active Directory Domain Services
- Command Prompt
- Windows 10 Domain Client

---

## Environment Setup

- **Server Name:** LAB-SRV-01
- **Domain:** LAB.local
- **Roles Installed:**  
  - Active Directory Domain Services  
  - DNS Server  
  - DHCP Server
- **Client Machine:** Windows 10 (Domain-joined)
- **Network Type:** VirtualBox Host-Only / Internal Network

---

## Steps Performed

### 1. Verified DNS Configuration

- Opened DNS Manager and confirmed the presence of the AD-integrated forward lookup zone:

"LAB.local"
- Verified A (Host) records for the domain and server.
- Confirmed the server was correctly resolving its own hostname.

**Screenshots included:** DNS Manager showing LAB.local zone and DNS records

---

### 2. Tested DNS Resolution

- Used `ipconfig /all` to verify the server was using itself as the DNS server.
- Used `ping LAB-SRV-01` to confirm name-to-IP resolution.

This confirmed DNS was functioning correctly before proceeding with DHCP configuration.

**Screenshots included:** ipconfig output and successful hostname ping

---

### 3. Installed DHCP Server Role

- Installed the DHCP Server role using Server Manager.
- Confirmed successful installation prior to configuration.

**Screenshot included:** DHCP Server role installation complete

---

### 4. Authorised DHCP Server in Active Directory

- Opened DHCP Manager.
- Authorised the DHCP server within Active Directory.
- Confirmed the server status was active and authorised.

This step is required in domain environments to prevent unauthorised DHCP servers.

**Screenshot included:** DHCP server authorised successfully

---

### 5. Created and Activated an IPv4 DHCP Scope

Created an IPv4 scope with the following configuration:

- **Scope Name:** LAB IPv4 Scope
- **IP Address Range:**  
"192.168.56.100 – 192.168.56.150"
- **Subnet Mask:**  
"255.255.255.0"

- **Lease Duration:** 8 days
- **DNS Server:** LAB-SRV-01
- **Router:** Not configured (lab environment)
- **Scope Status:** Activated

**Screenshots included:** IPv4 scope configuration and active scope

---

### 6. Tested DHCP Functionality from Client Machine

- Configured the Windows 10 client to obtain IP and DNS settings automatically.
- Released and renewed the IP configuration using:
"ipconfig /release
ipconfig /renew"

- Verified the client received:
- An IP address within the configured scope
- DHCP server listed as LAB-SRV-01
- DNS server set to the domain controller

- Confirmed the client appeared in DHCP address leases.

**Screenshots included:** Client IP configuration and DHCP lease list

---

## Outcome

- DNS verified and functioning correctly
- DHCP server installed and authorised
- IPv4 scope created and activated
- Client successfully received IP configuration via DHCP
- DNS and DHCP services confirmed working together within the domain

---

## What I Learned

- How DNS underpins Active Directory functionality
- How to verify DNS records and name resolution
- Why DHCP servers must be authorised in a domain
- How to configure and activate an IPv4 DHCP scope
- How to test and validate DHCP from a client machine
- The relationship between DNS, DHCP, and domain connectivity

---

## Why This Lab Matters

DNS and DHCP are core services in nearly all Windows-based networks. This lab demonstrates practical skills required for first-line and junior IT roles, including:

- Network troubleshooting
- Client connectivity issues
- Domain infrastructure support
- Safe and structured service configuration
- Validation of network services using real client testing

---

## Files & Screenshots

All screenshots related to this lab are stored in the `/screenshots` folder.
