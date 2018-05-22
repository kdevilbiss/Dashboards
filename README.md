# Dashboards

A collection of (tokenized) LogicMonitor dashboards that can be re-used across accounts. When importing, select the relevant group of devices for which you wish to visualize data. These are officially unsupported - but LogicMonitor support can always help with adjustments. 

Most of these dashboards rely on dynamic groups in the 'Devices by Type' device group - which can be created using the out-of-box PropertySources from LogicMonitor. (So make sure you have the latest PropertySources from the repository!)

Dashboard Names and expected dynamic group names:

Active Directory Overview
        Dynamic Group:      Device by Type/ Domain Controllers
        Group Definition:      hasCategory("MicrosoftDomainController")
Collector Summary
        Dynamic Group:      Device by Type/ Collectors
        Group Definition:      hasCategory("Collectors")
Exchange Server Overview
        Dynamic Group:      Device by Type/ Exchange Servers
        Group Definition:      hasCategory("MSExchange")
Local Network Latency
        Dynamic Group:      *
        Group Definition:      (Works without credentials for all devices)
Palo Alto Overview
        Dynamic Group:      Device by Type/ Palo Alto
        Group Definition:      hasCategory("PaloAlto")
SQL Server Overview
        Dynamic Group:      Device by Type/ SQL Servers
        Group Definition:      hasCategory("MSSQL")
Under Utilized Devices - On-Prem
        Dynamic Group:      *
        Group Definition:      (Point at the device group you wish to target)
Under Utilized Devices - Public Cloud
        Dynamic Group:      AWS or Azure account
        Group Definition:      (Requires a local collector to be installed and monitoring cloud VMs)
Web Server Overview
        Dynamic Group:      Device by Type/ Web Servers
        Group Definition:      hasCategory("MicrosoftIIS")

