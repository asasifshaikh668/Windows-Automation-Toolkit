# Hardware Health and Preventative Maintenance Scripts

This module contains a set of PowerShell scripts designed for proactive technical support. These tools retrieve internal hardware metrics that are often leading indicators of system stability issues or impending component failure.

----------------------------------------------------------------------------------------------------------

# Get-CPUTemperature.ps1 (CPU Temperature Check)

| Feature | Description |
|---|---|
| Script Title | Get-CPUTemperature.ps1 |
| Purpose | Queries the system's **WMI (Windows Management Instrumentation)** to estimate the CPU's current temperature. High temperatures indicate failing fans, dust buildup, or poor thermal paste application. |
| Core Commands | Get-WmiObject -Class Win32_PerfFormattedData_Counters_ThermalZoneInformation|
| Output | Provides the CPU temperature in both **Celsius (°C)** and **Fahrenheit (°F)**. Includes error handling for systems that do not expose this data. |
| Technical Support Value & Impact | Quick validation for performance issues and spontaneous shutdowns linked to thermal throttling. |
| How to Run | Run the script: .\Get-CPUTemperature.ps1. Admin rights is required to run the cript.|

----------------------------------------------------------------------------------------------------------
