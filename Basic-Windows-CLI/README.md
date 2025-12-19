# Lab 2 — Basic Windows Command Line & PowerShell

## Lab Objective
Demonstrate practical use of Windows Command Prompt and PowerShell to gather system information, test connectivity, and inspect running processes and services in a Windows environment.

---

## Scenario
A support technician needs to collect system and network information from a Windows workstation, verify internet connectivity, and review running processes and services using command-line tools.

---

## Environment
- **Operating System:** Windows 11  
- **Device Type:** Workstation  
- **Tools Used:**
  - Command Prompt (run as Administrator)
  - PowerShell (run as Administrator)

---

## Investigation Steps

### 1. Network Configuration (Command Prompt)
Ran the following command:
"ipconfig"

Reviewed:
- IP address
- Default gateway

This confirmed the system had valid network configuration.

---

### 2. Internet Connectivity Test
Ran:
"ping google.com"

This verified that the system could reach an external host, confirming basic internet connectivity.

---

### 3. Network Path Analysis
Executed:
tracert google.com

This displayed the route taken by network traffic, helping identify where connectivity issues may occur if a failure is present.

---

### 4. System Information Review
Ran:
"systeminfo"

Collected:
- Operating system version
- Installed memory
- System uptime
- Patch and update information

This provided a high-level overview of system health and configuration.

---

### 5. Process Inspection (PowerShell)
Opened PowerShell and ran:
"Get-Process"

Reviewed all active applications and background processes to understand system workload.

---

### 6. Service Status Review (PowerShell)
Executed:
"Get-Service"

Checked:
- Running services
- Stopped services

This is useful for identifying service-related issues during troubleshooting.

---

### 7. Detailed System Information (Optional)
Ran:
"Get-ComputerInfo"

Retrieved detailed hardware and operating system information for deeper diagnostics.

---

## Verification
- Network configuration successfully retrieved via CLI  
- Internet connectivity confirmed  
- Network routing information obtained  
- System details collected using command-line tools  
- Running processes and services successfully reviewed  

---

## Outcome
The system’s network status, connectivity, and operational state were successfully verified using Command Prompt and PowerShell.

---

## Key Takeaways
- How to use Command Prompt and PowerShell for system diagnostics  
- How to retrieve network and system information using CLI tools  
- How to test connectivity and trace network paths  
- Differences between CMD and PowerShell use cases in IT support  

---

## Evidence
Screenshots documenting each step are stored in the `/screenshots` directory, including:
- Command Prompt opened as Administrator  
- Output of `ipconfig`  
- Output of `ping google.com`  
- Output of `tracert google.com`  
- Output of `systeminfo`  
- PowerShell session opened  
- Output of `Get-Process`  
- Output of `Get-Service`  
- (Optional) Output of `Get-ComputerInfo`
