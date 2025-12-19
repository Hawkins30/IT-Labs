# Lab 3 — Hardware Troubleshooting (Disk Performance Issue)

## Lab Objective
Demonstrate a structured approach to diagnosing and resolving system performance issues caused by hardware and storage constraints in a Windows environment.

---

## Scenario
A user reports that their Windows 11 laptop is extremely slow. Applications take a long time to open, and the system occasionally freezes for several seconds during normal use.

---

## Environment
- **Operating System:** Windows 11  
- **Device Type:** Laptop  
- **User Context:** Single-user workstation  
- **Tools Used:**
  - Task Manager
  - Windows Event Viewer
  - Storage Settings
  - Disk Cleanup
  - Windows Security

---

## Symptoms Observed
- Slow overall system performance  
- Long application load times  
- Intermittent system freezing  
- Disk usage consistently near 100% in Task Manager  

---

## Investigation Steps
1. Checked CPU, memory, and disk usage using Task Manager.  
2. Identified sustained high disk utilisation despite minimal application activity.  
3. Reviewed Storage Settings and confirmed less than 2GB of free disk space.  
4. Examined Event Viewer logs and found warnings related to low disk space and disk performance.  

---

## Root Cause
The system was critically low on available storage. Windows relies on free disk space for virtual memory (pagefile operations). With insufficient free space, disk I/O became saturated, resulting in severe performance degradation.

---

## Resolution Steps
1. Ran Disk Cleanup to remove temporary and unnecessary system files.  
2. Uninstalled unused applications consuming significant storage.  
3. Moved large personal files (photos and videos) to cloud storage.  
4. Restarted the system to apply changes and reset system resources.  

---

## Verification
- Free disk space increased from approximately **1.8GB to 21GB**  
- Disk utilisation returned to normal operating levels  
- System responsiveness improved significantly  
- No further freezing observed after reboot  

---

## Outcome
The user’s system performance returned to normal, with stable disk usage and improved responsiveness during everyday tasks.

---

## Key Takeaways
- Low disk space can cause high disk usage and system instability  
- Task Manager and Event Viewer are effective tools for diagnosing performance issues  
- Maintaining adequate free storage is critical for Windows system health  

---

## Evidence
Screenshots documenting each stage of diagnosis and resolution are stored in the `/screenshots` directory, including:
- Task Manager showing high disk usage  
- Storage settings showing low available disk space  
- Disk Cleanup execution  
- Post-fix system performance

