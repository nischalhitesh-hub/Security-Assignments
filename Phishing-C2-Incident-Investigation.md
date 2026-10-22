# Phishing and C2 Incident Investigation
## Overview
Simulated real time SOC investigations using SPLUNK triaging a live alert queue that revealed a full attack chain.
### Attack Chain
Initial access via phishing email with malicious Zip attachment, powershell script dropped to disk as payload, DNS based command and control beakoning via nslookup to a suspicious domain.
### Exfiltration Data
Prepared and copied via robocopy.exe to a mapped network drive which was later disconnected to cover tracks.
### Distinguished True positives from false positives
By recognising legitimate windows system behaviour. Like 'Trustedinstaller.exe' and schedule tasks like KEYROAMING and NGC KEY PREGEN vs geniunely malicious parent child processes. 
### Remediation Actions
Isolated the affected host from the network to stop further exfiltration, blocked the malicious C2 domain and suspicious email sender domain, quarantined phishing emails and attachment, reset credentials for the compromised user account, recommended forensic review of the file share access logs to scope the full extent of data exfiltration.
### Skills and Tools demonstrated
Splunk and SIEM alert triage, Phishing email analysis, windows process and sysmon log analysis, DNS based command and control detection, incident documentation and reporting.

## Overall Analysis

<img width="1315" height="654" alt="Screenshot 2026-10-22 at 3 00 05 PM" src="https://github.com/user-attachments/assets/c6c6a875-8005-4f2b-9c65-2a6f683c3700" />

## Incident Report

<img width="1110" height="650" alt="Screenshot 2026-10-22 at 1 42 05 PM" src="https://github.com/user-attachments/assets/eb0aa822-eb02-4199-8770-91ddcdf832d2" />

## Final Result 

<img width="1386" height="678" alt="Screenshot 2026-10-22 at 2 59 32 PM" src="https://github.com/user-attachments/assets/fb372707-3823-4158-bab0-e1c6812575a9" />








