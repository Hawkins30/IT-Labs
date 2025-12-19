# Lab 4 — Basic Networking (IP Address, DNS, and Default Gateway)

## Lab Objective
Demonstrate a structured approach to identifying and verifying basic network configuration on a Windows system, including IP addressing, DNS configuration, default gateway, and connectivity testing.

---

## Scenario
A user reports potential network connectivity issues and requires verification of their network configuration and internet access. The task is to confirm that the device is correctly configured and can communicate both within the local network and with external resources.

---

## Environment
- **Operating System:** Windows 11  
- **Device Type:** Workstation  
- **Network Type:** Local Area Network (LAN)  
- **Tools Used:**
  - Command Prompt
  - Windows Network Settings

---

## Investigation Steps

### 1. Viewing Network Adapter Information
Opened Command Prompt and ran:
"ipconfig"

Reviewed the following:
- IPv4 address  
- Subnet mask  
- Default gateway  

This confirmed the device had a valid IP address assigned.

---

### 2. Viewing DNS Server Configuration
Ran:
"ipconfig /all"

Verified:
- DNS server addresses  
- DHCP server  
- Full network adapter configuration  

This confirmed DNS was correctly assigned via DHCP.

---

### 3. Verifying Network Settings via GUI
Navigated to:
"Settings → Network & Internet → Properties (active connection)"

Confirmed:
- Connection type  
- IPv4 address  
- Default gateway  
- DNS server configuration  

This ensured GUI and CLI configurations matched.

---

### 4. Testing Internet Connectivity
Executed the following commands:
"ping 8.8.8.8"
"ping google.com"

Results:
- Successful ping to `8.8.8.8` confirmed external network connectivity  
- Successful ping to `google.com` confirmed DNS resolution was working  

---

### 5. Testing Default Gateway Reachability
Pinged the default gateway:
"ping <gateway IP>"
(e.g. `ping 192.168.1.1`)

A successful response confirmed local network connectivity.

---

## Verification
- Device received a valid IP address  
- DNS servers were correctly assigned  
- Default gateway was reachable  
- Internet connectivity confirmed  
- DNS resolution functioning as expected  

---

## Outcome
The system was confirmed to be correctly configured for network access, with full local and internet connectivity.

---

## Key Takeaways
- How to identify IP address, DNS servers, and default gateway  
- Difference between local network connectivity and internet connectivity  
- How to test DNS functionality using command-line tools  
- How to verify network configuration using both CLI and GUI methods  

---

## Evidence
Screenshots documenting each step are stored in the `/screenshots` directory, including:
- `ipconfig` output  
- `ipconfig /all` showing DNS configuration  
- Network & Internet Properties window  
- Successful ping to `8.8.8.8`  
- Successful ping to `google.com`  
- Successful ping to the default gateway  
