# 100-days-challenge-day-5

The server behind it may not be. By performing a Reverse IP lookup, I identified multiple websites hosted on the same server. One weak website can compromise others on shared hosting, which is a common real-world attack scenario."

Reverse IP Lookup & Shared Hosting Attack Surface  

Overview

I explored how a website’s apparent security does not necessarily reflect the security of the server infrastructure behind it. 
 
Using Reverse IP lookup, I enumerated multiple domains resolving to the same IP address, exposing a shared hosting environment.

This exercise demonstrates a common real-world attack scenario where a single vulnerable website can be leveraged to compromise other co-hosted sites due to weak isolation, misconfigurations, or improper access controls.

Key Concept: Reverse IP Lookup

Reverse IP lookup is an OSINT and reconnaissance technique used to:

Identify all domains hosted on a single IP address

Map shared infrastructure

Assess potential blast radius of a server-level compromise

In shared hosting environments, multiple unrelated websites often run under the same server, increasing systemic risk.

Security Risk in Shared Hosting

If one hosted application is vulnerable (e.g., outdated CMS, insecure file uploads, weak permissions), an attacker may:

Exploit the vulnerable site
 
Deploy a web shell
 
Escalate privileges
 
Move laterally to neighboring virtual hosts

This makes shared hosting a frequent target in real-world attacks.

MITRE ATT&CK Mapping

The following MITRE ATT&CK techniques align with this scenario:

Reconnaissance
 
T1596 – Search Open Technical Databases

Reverse IP lookups rely on public datasets and OSINT sources to enumerate domains associated with an IP.

Target Profiling
 
T1589 – Gather Victim Identity Information (Infrastructure Context)

Identifying related domains helps profile the hosting environment and attack surface.

Initial Access
 
T1190 – Exploit Public-Facing Application

A vulnerable website on the shared server can provide the initial foothold.

Persistence
 
T1505.003 – Web Shell

Web shells may be deployed to maintain persistent access to the compromised host.

Privilege Escalation

T1068 – Exploitation for Privilege Escalation

Misconfigurations or vulnerable services can allow attackers to escalate privileges beyond the web user.

Lateral Movement

T1021 – Remote Services (Shared Infrastructure Context)

Poor isolation can allow access to neighboring virtual hosts or services.

Impact

T1496 – Resource Hijacking

Compromised servers may be abused for cryptomining, spam campaigns, or malware hosting.
  
T1498 – Network Denial of Service (Indirect Risk)

One compromised site can result in IP blacklisting or service disruption for all hosted domains.

Defensive Takeaways

To mitigate shared hosting risks:

Enforce strict file and user permission separation
 
Keep CMS, plugins, and server software updated
 
Disable unnecessary services

Implement proper containerization or virtualization
 
Monitor logs for abnormal lateral activity

Key Takeaway

Reverse IP lookup provides infrastructure-level visibility, revealing shared hosting risks where a single vulnerable website can lead to multi-site compromise.

Progress

Day 5 of 100 Days of Hacking  
 
Focus: OSINT · Infrastructure Recon · MITRE ATT&CK Mapping

#OSINT #Reverse-IP #CyberSecurity #EthicalHacking  
#MITRE-ATTACK #Shared-Hosting #Reconnaissance  
#100DaysOfHacking

Academy : SKILLS UPRISE

Mentor: Manoj kumar Koravangi

