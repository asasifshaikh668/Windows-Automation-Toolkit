**Script: Invoke-SystemDiagnostics.bat**

This script is designed to rapidly diagnose and proactively address common causes of Windows system slowness in a single execution. It significantly reduces the time spent manually collecting performance data and running standard maintenance tasks during a support ticket lifecycle.

| Category | Command/Function | Purpose & Value |
| :--- | :--- | :--- |
| Initial Assessment | wmic cpu get load percentage, wmic os get physical memory, wmic logical disk get size,freespace,caption | ollects baseline metrics (CPU, RAM, Disk space/free space) to immediately identify hardware bottlenecks (e.g., low RAM or full disk) before running repairs. |
| Running Processes | Tasklist | Identifies resource-intensive, unauthorized, or runaway processes that may be consuming excessive resources, leading to slowness. |
| Startup Optimization | wmic startup get caption,command | Lists applications configured to run at startup, enabling identification of unnecessary programs slowing down boot time and initial login. |
| Cleanup | Cleanmgr /d C:, Rmdir /s /q %temp% | Executes built-in Disk Cleanup utility and removes temporary files (%temp%), reclaiming disk space and improving read/write speeds. |
| System Integrity Checks | sfc /scannow, Dism /online /cleanup-image /restorehealth | Runs System File Checker (SFC) and Deployment Image Servicing and Management (DISM) to repair corrupted system files and restore the health of the Windows component store. |
| File System Health | Defrag C: /U /V, Chkdsk /f/r | Optimizes file structure (defragmentation) for mechanical drives and checks/repairs the file system structure (CHKDSK), addressing disk-related performance degradation. |


**Technical Support Value & Impact**

* **Time Reduction:** Automates over 10 separate manual commands, saving an estimated **15–20 minutes** per troubleshooting session.
* **Proactive Repair:** Unlike manual diagnosis, this script immediately initiates repair steps (sfc, Dism, Cleanmgr), often resolving performance issues without further technician interaction.
* **Standardization:** Ensures every system slowness ticket is diagnosed and treated using the same **best-practice methodology**.

----------------------------------------------------------
**How to Run**

1. Download the script to the target Windows machine.
2. Open Command Prompt as an Administrator.
3. Execute the script:
   
   ```.\Invoke-SystemDiagnostics.bat```
   
*Note: Script execution may take several minutes due to comprehensive tasks like CHKDSK and SFC.*
