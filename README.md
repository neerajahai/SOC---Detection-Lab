# SOC---Detection-Lab
A hands-on SOC detection environment built using Splunk, Ubuntu, and Kali Linux. This lab demonstrates log collection, Universal Forwarder setup, Nmap/SSH brute force attack simulations, and creation of SPL detection queries for security monitoring and analysis.
In this lab, I built a basic SOC detection environment to simulate real-world attack detection using Splunk.

Lab Environment

Attacker Machine: Kali Linux

Target / Log Source: Ubuntu Linux

SIEM: Splunk Enterprise

Log Collection: Splunk Universal Forwarder

Network: VirtualBox (Host-Only / NAT)

  Activities Performed :
  
1.Log Collection Setup

Installed and configured Splunk Enterprise on Ubuntu

Installed Splunk Universal Forwarder to collect Linux system logs

Configured log inputs to monitor:
  /var/log/auth.log
  /var/log/syslog
Verified logs were successfully indexed in Splunk

2.Attack Simulation

Performed Nmap scans from Kali Linux to identify open services, Simulated SSH brute-force attempts against the Ubuntu machine , Generated multiple authentication failure events in system logs

3. Detection & Analysis in Splunk

Analyzed Linux authentication logs in Splunk
Identified SSH attack indicators such as:
   Failed password
    Invalid user
Created SPL detection queries to:
  Filter SSH authentication failure, Extract attacker source IP addresses, Count repeated failed attempts per IP

4. Alert Creation
  Built a SSH Brute Force detection alert using SPL, Configured alert thresholds based on repeated failed login attempts, Verified alert functionality by triggering attacks from Kali Linux.

  Key Detection Use Case

  SSH Brute Force Attack Detection
  Detection based on multiple failed SSH login attempts from a single IP within a short time window

Outcome:

  This lab demonstrates:
End-to-end SOC workflow (Attack → Log → Detection → Alert)
Practical experience with Splunk SPL
Realistic blue-team detection techniques for Linux environments

## 📸 Detection Screenshots

![SSH Failed Events](screenshots/Splunk_ssh_failed_events.png)
