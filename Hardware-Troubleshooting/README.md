# Lab 3 — Hardware Troubleshooting Case Study

## Issue Description
A user reports that their Windows 11 laptop has become extremely slow. Applications take a long time to open, and the system sometimes freezes for several seconds.

## Symptoms Observed
- Slow system performance  
- Long application load times  
- Occasional system freezing  
- High disk usage shown in Task Manager  

## Tools Used for Diagnosis
- Task Manager  
- Windows Event Viewer  
- Storage Settings  
- Disk Cleanup  
- Windows Security Scan  

## Steps Taken to Diagnose the Problem
1. Opened **Task Manager** and checked CPU, RAM, and Disk usage.  
2. Observed **Disk usage at 100%**, even when no heavy apps were running.  
3. Checked **Storage** and saw the device had less than 2GB free space.  
4. Opened **Event Viewer** and found warnings about disk fragmentation and low disk space.  

## Root Cause
The laptop was extremely low on available storage. Windows uses disk space for virtual memory (pagefile), so when storage is nearly full, performance becomes extremely slow.

## Steps Taken to Fix the Problem
1. Ran **Disk Cleanup** and removed temporary files.  
2. Uninstalled unused applications taking up large amounts of space.  
3. Moved large personal files (videos/photos) to cloud storage.  
4. Restarted the system.

## Outcome
- Available storage increased from 1.8GB → 21GB  
- Disk usage dropped to normal levels  
- System performance returned to normal  
- No freezing or slowdowns after reboot  

## What I Learned
- Low disk space can cause 100% disk usage and severely impact performance  
- How to diagnose system slowness using Task Manager  
- How Windows uses the pagefile and why storage matters  
- How to perform basic system cleanup to restore performance  

## Screenshots
All screenshots are saved in the `screenshots` folder and include:
- Task Manager showing high disk usage  
- Storage menu showing low disk space  
- Disk Cleanup window  
- After-fix screenshot showing normal disk usage  
