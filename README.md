**Windows SOC Sysmon Lab**
Overview

This project demonstrates a hands-on Windows SOC lab focused on endpoint visibility, attacker tradecraft detection, and log analysis using Sysmon.

A Windows 10 virtual machine was instrumented with Sysmon using a custom configuration to capture high-fidelity endpoint telemetry. Suspicious PowerShell activity was then generated and detected via Sysmon process creation events.

**Tools & Technologies**

Windows 10 (VirtualBox)

Sysmon (Sysinternals)

Custom Sysmon configuration (process creation logging)

Windows Event Viewer

**Lab Setup**

Deployed a Windows 10 VM in VirtualBox

Configured advanced Windows auditing policies

Installed Sysmon with a custom configuration file

Verified telemetry collection via Event Viewer

**Detection Scenario**

To simulate attacker behavior, PowerShell was executed using common malicious flags:

-ExecutionPolicy Bypass

-NoProfile

Hidden window execution

Sysmon Event ID 1 (Process Create) successfully captured:

Process name (powershell.exe)

Full command-line arguments

User context and timestamp

**Analysis**

The detected PowerShell command-line behavior is commonly associated with:

Malware execution

Fileless attacks

Living-off-the-land techniques (LOLBins)

This demonstrates how endpoint telemetry can be used by SOC analysts to identify suspicious activity even without traditional antivirus alerts.

**Evidence**

Screenshots documenting:

VM environment

Sysmon installation

Captured Sysmon Event ID 1 showing suspicious PowerShell execution

(See /screenshots folder)

**Key Takeaways**

Built foundational SOC skills using endpoint telemetry

Learned how attackers abuse PowerShell

Practiced identifying suspicious behavior through log analysis

Gained experience documenting security findings
