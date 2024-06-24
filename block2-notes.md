VMO NOTES - BLOCK 2
===================

Contents
--------

> Insights

> L1 - ACAS Overview

> L2 - ACAS Hierarchy Structure

> L3 - ACAS Tool Functions

> L4 - ACAS Administrator Responsibilities

> L5 - Role-based Access Control

> L6 - DEMO - Role-based Access Control

> L7 - ACAS Repository Functions

> L8 - ACAS Repositories

> L9 - DEMO - ACAS Repositories

> L10 - ACAS Active Scan Objects

> L11 - ACAS Active Scan Management: Nessus Scanner

> L12 - DEMO - ACAS Active Scan

> L13 - Queries & Reports: Demo Query within ACAS

> L14 - Queries & Reports: Demo Reports within ACAS

> L15 - ACAS Self-Diagnosis

---

<br>

## Insights

> - 

---

<br>

## L1 - ACAS Overview

> - Goals
>   - Differentiate the tools within the ACAS tool suite
>   - Describe purpose of Repositories with ACAS
>   - Define definition of Plugins within ACAS
>   - Discuss function of Plugins within ACAS
>   - Discuss ACAS Capabilities and Limitations

> - ACAS Tools/Software Components
>   - Tenable.sc (previously Security Center)
>       - Central console for ACAS. Offers automation & scale vulnerability/compliance scanning infrastructure. Allows management, altering, & reporting against vulnerability/compliance requirements
>   - Nessus Scanner
>       - Covers a breadth of checks, including unique CVEs, & operates across different environments. Can meet active scan requirements
>   - Nesus Network Monitor (NNM)
>       - Monitors network traffic in real-time, determining client & server vulnerabilities & sending them to Tenable. Continuously looks for new hosts, applications, & vulnerabilities w/o active scanning. Can meet passive scan requirements
>   - Nessus Manager
>       - Manager for Nessus agents & linked to Tenable, allowing Tenable to query the manager for agent scans. Can meet active scan requirements
>   - Nessus Agents
>       - Installed locally on a host, collecting vulnerability, compliance, & system data, & reports that info to a manager. Can perform Non-Credentialed scans on hosts, offline assets, & endpoints that intermittently connect to the internet
>   - Log Correlation Engine (LCE)
>       - Server
>           - Collects & normalizes data from clients, which is then analyzed using Tenable. Both raw & normalized data are available to the user
>       - Interface
>           - Web-based interface provided by each LCE server, for monitoring LCE server/client health & status, configuring LCE servers, managing clients, creating & assigning policies, & managing users
>       - Clients
>           - Installed on hosts to monitor & collect events, which are sent to the LCE Server and are both stored as raw logs & normalized & correlated with vulnerabilities

> - Repositories
>   - *"Scan data is stored in a proprietary data file format called a repository"*
>   - When a scan is initiated, results are imported into a repository
>   - Data is retained according to Admin-defined expiration settings
>   - Repositories are defined by an IP range or the Mobile Device Manager (MDM) data type they accept
> - 2 Categories, 5 Types
>   - Local - IPv4, IPv6, Mobile
>   - External - Remote, Offline

> - ACAS Plugins Defined
>   - Developed by Tenable Research to detect new vulnerabilities
>   - Written in the proprietary Nessus Attack Scripting Language (NASL)
>   - Contain vulnerability information, simplified remediation actions, & the algorithm to test for vulnerability presence
>   - Families - Named by attack type, device family, or plugin action; used to manage large groups of plugins, enabling/disabling potentially thousands of plugins, with the option to manually enable or disable specific plugins within a family
>       - Backdoors
>       - CISCO
>       - Databases
>       - Denial of Service
>           - Will be executed when Safe Checks are disabled
>       - Firewalls
>           - Deals with firewall devices & software that don't have a specified family
>       - Gain a shell remotely
>       - Port Scanners
>       - SCADA
>       - Service Detection
>           - Plugins that detect specific protocol or application listening on a port
>       - Web Servers
>       - Windows
>       - Windows: User Management
>           - Local security checks that specifically cover user information
>   - Categories for specific protocols
>       - DNS
>       - FTP
>       - RPC (Remote Procedure Call)
>       - SMTP
>       - SNMP (Simple Network Management Protocol)

> - Functions of ACAS Plugins
>   - Plugins typically cover 1 or more CVE IDs, allowing an ACAS scan to detect new vulnerabilities
>   - Configure Plugin Options
>       - Required User Role: Admin or organizational user w/ permissions
>       - VMO can configure plugin options within a scan policy to enable or disable them on a family or individual level

> - ACAS Capabilities
>   - Nessus Scanner Capabilities
>       - Agentless
>       - Scalable Solution
>       - Vulnerability Scanning
>       - Network Discovery
>           - Perform mandated discovery scans
>           - ID computers, server, printers, switches, routers, & IP phones on base
>       - Compliance Reporting
>           - Perform mandated compliance scans of security configuration checks
>   - Nessus Scanner Limitations
>       - Does not remediate vulnerabilities
>       - Shared resources among multiple bases limits concurrent data import
>       - Scans can be time-consuming
>       - Scans can utilize high network bandwidth
>       - Scans only for known vulnerabilities
>       - Most mandated scans require credentials

---

<br>

## L2 - ACAS Hierarchy Structure

> - 