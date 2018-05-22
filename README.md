# Dashboards

A collection of (tokenized) LogicMonitor dashboards that can be re-used across accounts. When importing, select the relevant group of devices for which you wish to visualize data. These are officially unsupported - but LogicMonitor support can always help with adjustments. 

Most of these dashboards rely on dynamic groups in the 'Devices by Type' device group - which can be created using the out-of-box PropertySources from LogicMonitor. (So make sure you have the latest PropertySources from the repository!)

**Dashboard Names | Expected dynamic group names | Group definitions:**

Active Directory Overview | Device by Type/ Domain Controllers | hasCategory("MicrosoftDomainController")
        
Collector Summary | Device by Type/ Collectors | hasCategory("Collectors")

Exchange Server Overview | Device by Type/ Exchange Servers | hasCategory("MSExchange")

Local Network Latency | * | (Works without credentials for all devices)

Palo Alto Overview | Device by Type/ Palo Alto | hasCategory("PaloAlto")

SQL Server Overview | Device by Type/ SQL Servers | hasCategory("MSSQL")

Under Utilized Devices - On-Prem | * | (Point at the device group you wish to target)

Under Utilized Devices - Public Cloud | AWS or Azure account | (Requires a local collector to be installed and monitoring cloud VMs)

Web Server Overview | Device by Type/ Web Servers | hasCategory("MicrosoftIIS")
