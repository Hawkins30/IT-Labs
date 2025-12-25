# Lab — Windows Server 2022: Active Directory User Logon & Group Policy Troubleshooting

## Purpose

The purpose of this lab is to deploy a Windows Server 2022 Domain Controller, create domain users and groups, apply Group Policy logon rights, and troubleshoot a real-world domain logon failure. This lab demonstrates practical Active Directory administration and Group Policy troubleshooting skills commonly required in IT support, service desk escalation, and junior system administrator roles.

---

## Tools Used

- Windows Server 2022 Standard (Evaluation)
- Oracle VirtualBox
- Active Directory Domain Services (AD DS)
- Group Policy Management Console (GPMC)
- Active Directory Users and Computers (ADUC)
- Command Prompt (Administrator)

---

## Environment Setup

- **Server Name:** LAB-SRV-01  
- **Domain Name:** lab.local  
- **Role Installed:** Active Directory Domain Services  
- **Server Role:** Domain Controller  

The server was installed from ISO, updated fully, renamed, and promoted to a Domain Controller.

---

## Steps Performed

### 1. Installed and Promoted Domain Controller

- Installed the **Active Directory Domain Services** role.
- Promoted the server to a **new forest**:
"lab.local"
- Restarted and confirmed Domain Controller functionality.

**Screenshot included:** Domain Controllers OU visible

---

### 2. Created Domain User and Security Group

- Created domain user:
"john.smith"
- Created security group:
"IT-Support"
- Added **john.smith** to the **IT-Support** group.

**Screenshot included:** User group membership

---

### 3. Identified Logon Failure

Attempting to log in as **john.smith** resulted in the following error:

> “The sign-in method you’re trying to use isn’t allowed.”

This confirmed a **logon rights policy restriction**, not an account, password, or domain join issue.

**Screenshot included:** Logon error message

---

### 4. Investigated Group Policy Scope

- Reviewed **Default Domain Policy**
- Identified that **logon rights on Domain Controllers** are governed by:
"Default Domain Controllers Policy"
- Confirmed that policies affecting Domain Controllers must be applied at the **Domain Controllers OU**, not the domain root.

This reflects a common real-world Active Directory misconfiguration.

---

### 5. Corrected Logon Rights Policy

Edited **Default Domain Controllers Policy**:

"Computer Configuration
→ Policies
→ Windows Settings
→ Security Settings
→ Local Policies
→ User Rights Assignment
→ Allow log on locally"

Added the following:
- Administrators
- Domain Admins
- IT-Support

Applied the policy successfully.

**Screenshot included:** Allow log on locally policy

---

### 6. Verified Group Policy Application

Ran the following command:
"gpresult /r"

Confirmed:
- Default Domain Controllers Policy applied successfully
- No conflicting Group Policies present

**Screenshot included:** gpresult output

---

### 7. Successful Domain Login

- Successfully logged in as:
"LAB\john.smith"
- Confirmed domain authentication and desktop access.

**Screenshot included:** Successful domain login

---

## Outcome

- Domain Controller deployed and operational
- Active Directory users and groups configured
- Group Policy applied at the correct scope
- Logon restriction diagnosed and resolved
- Domain user successfully authenticated

---

## What I Learned

- How logon rights are enforced differently on Domain Controllers
- The difference between **Default Domain Policy** and **Default Domain Controllers Policy**
- How to diagnose “sign-in method not allowed” errors
- How to verify applied Group Policies using `gpresult`
- How to troubleshoot authentication issues methodically in Active Directory environments

---

## Why This Lab Matters

This lab mirrors real enterprise troubleshooting scenarios where:

- User accounts are enabled but logon fails
- Group Policy is applied at the wrong scope
- Domain Controller security policies override domain-level settings

Understanding these distinctions is critical for IT support, service desk escalation, and junior system administrator roles in Windows enterprise environments.

---

## Files & Screenshots

All screenshots for this lab are stored in the `/screenshots` folder.
