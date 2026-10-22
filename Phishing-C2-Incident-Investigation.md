#Phishing and C2 Incident Investigation
##Overview
Simulated real time SOC investigations using SPLUNK triaging a live alert queue that revealed a full attack chain.
###Attack Chain
Initial access via pshishing email with malicious Zip attachment, powershell script dropped to disk as payload, DNS based command and control beakoning via nslookup to a suspicious domain.
###Exfiltration Data prepared and copied via robocopy.exe to a mapped network drive which was later disconnected to cover tracks.
###Distinquished True positives from false positives by recognising legitimate windows system behaviour. Like 'Trustedinstaller.exe' and schedule tasks like KEYROAMING and NGC KEY PREGEN vs geniunely malicious parent child processes. 
###Remidiation Actions: Isolated the affected host from the network to stop further exfiltration, blocked the malicious C2 domain and suspicious email sender domain, quarantined phishing emails and attachment, reset credentials for the compromised user account, recommended forensic review of the file share access logs to scope the full extent of data exfiltration.
###Skills and Tools demonstrated
Splunk and SIEM alert triage, Phishing email analysis, windows process and sysmon log analysis, DNS based command and control detection, incident documentation and reporting.
