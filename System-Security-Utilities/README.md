# 🧹 Cleanup-TempFiles
_**Script: Cleanup-TempFiles.ps1 & Cleanup-TempFiles.bat**_

| Section | Content |
|---|---|
| Script Title | Cleanup-TempFiles.ps1 & Cleanup-TempFiles.bat |
| Description | Cleanup-TempFiles is a dual-script utility (PowerShell & Batch) designed to reclaim disk space and resolve common Windows update errors. It aggressively targets temporary user data, system logs, and the Windows Update download cache. |
| Features | ***Temp File Removal:** Deletes data from ```%TEMP%``` and ```C:\Windows\Temp``` to free up space. ***Windows Update Reset:** Stops the ```wuauserv``` service and flushes the ```SoftwareDistribution``` cache to fix stuck updates. ***Recycle Bin Purge:** Forces the Recycle Bin to empty immediately.  ***Browser Cache:** Clears standard browser temporary files located in system temp folders. |
| Usage Instructions | **⚠️ Administrator Privileges Required** > These scripts must be run as ```Administrator``` to access system folders like ```C:\Windows\Temp``` and ```SoftwareDistribution```. **⚠️ Disclaimer:** This script permanently deletes files. While it targets temporary data, always ensure you have saved your work before running.|

********************************************************************************************************
