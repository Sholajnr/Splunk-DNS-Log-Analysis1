# Splunk-DNS-Log-Analysis1
Hands-on SOC Investigation using Splunk SIEM to analyze DNS traffic, identify suspicious domains, and investigate network activity
Project Overview
This project demonstrates hands-on SOC Analyst experience using Splunk Enterprise SIEM to investigate DNS network traffic, identify unusual DNS queries, and analyze potential security threats.
Tools Used - Splunk Enterprise 10.4.3
Splunk Search Processing Language (SPL)
Zeek DNS Logs
Windows
Regular Expressions (Regex)
Dataset Information
Log File: dns.log
Index: main
Source Type: dns
Total Events: 422,130
Project Objectives
Upload and analyze DNS logs using Splunk.
Extract source IP addresses, destination IP addresses, and DNS queries.
Identify the most frequently queried domains.
Investigate potentially suspicious DNS activity.
Develop practical SOC investigation skills.
Splunk Investigation
1. DNS Log Analysis
Used the following SPL query to retrieve DNS events:

index=main sourcetype=dns

2. DNS Field Extraction
Used regular expressions to extract important DNS information, including source IP addresses, destination IP addresses, and queried domains.

3.** Top DNS Queries**
Used SPL to identify frequently queried domains:

| stats count by dns_query
| sort -count
| head 20

4. Preliminary Findings
Observed DNS queries associated with services including Microsoft, Google, Apple, and Norton.

Identified unusual query strings that require further investigation.

No malicious activity has been confirmed at this stage.

Skills Demonstrated
SIEM log ingestion
DNS traffic analysis
SPL querying
Regular expression field extraction
Security monitoring
SOC investigation
Project Status
In Progress

Next Steps
Investigate suspicious DNS domains.
Analyze DNS query frequency.
Identify failed DNS requests.
Investigate possible command-and-control activity.
Document investigation findings.
