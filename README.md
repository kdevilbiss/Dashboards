# Dashboards

A collection of (tokenized) LogicMonitor dashboards that can be re-used across accounts. When importing, change the value of the ##defaultResourceGroup## (or ##defaultDeviceGroup##) token to select the relevant group of devices for which you wish to visualize data. Intended to be examples to get the creativity flowing! (LogicMonitor Support can always help with adjustments)

These dashboards largely   rely on both the latest versions of LogicMonitor datasources, and dynamic groups in the 'Devices by Type' device group. If these groups don't exist, they can be created using the out-of-box PropertySources from LogicMonitor together with the below documentation. [So make sure you have the latest PropertySources (and DataSources) from the repository!](https://www.logicmonitor.com/support/settings/logicmodules/keeping-your-datasources-up-to-date/)

To see a preview of what some of these dashboards look like, visit the [LogicMonitor Dashboard Gallery](https://www.logicmonitor.com/sales/dashboards/index.html).

**Default Dashboards 2.0 Names | Expected dynamic group names | Group definitions:**

- Alerts | * | (Works without credentials for all devices)
- Collectors | Devices by Type/ Collectors | hasCategory("Collectors")
- Hyper-V | Devices by Type/ Hyper-V | hasCategory("HyperV")
- Linux | Devices by Type/ Linux Servers | isLinux()
- Local Network Latency | Devices by Type/* | (Works without credentials for all devices)
- Network | Devices by Type/ Network | isNetwork()
- NOC Alert Map | Devices by Type/ * | (Works via location property on devices)
- Resource Utilization | Devices by Type/* | *
- SQL Server | Devices by Type/ SQL Servers | hasCategory("MSSQL")  *For the latest JDBC MSSQL DataSources*
- VMware vCenter | Devices by Type/ VMware Hosts | system.virtualization =~ "VMware ESX Host"
- Welcome to LogicMonitor | * | (Works without credentials for all devices)
- Windows | Devices by Type/ Windows Servers | isWindows()

**Microsoft Suite 1.0 | Expected dynamic group | Group definitions:**

- Active Directory | Devices by Type/ Domain Controllers | hasCategory("MicrosoftDomainController")
- DHCP Servers | Devices by Type/ Windows Servers | isWindows()
- DNS Servers | Devices by Type/ Windows Servers | isWindows()
- Exchange Server | Devices by Type/ Exchange Servers | hasCategory("MSExchange")
- Failover Clustering | Devices by Type/ Windows Servers | isWindows()
- File Server | Devices by Type/ Windows Servers | isWindows()
- Hyper-V 2012 R2 | Devices by Type/ Hyper-V | hasCategory("HyperV")
- Hyper-V 2016 | Devices by Type/ Hyper-V | hasCategory("HyperV") * (Requires updated Hyper-V datasources)
- IIS | Devices by Type/ Web Servers | hasCategory("MicrosoftIIS")
- Microsoft .NET Framework | Devices by Type/ Windows Servers | isWindows()
- Microsoft Message Queue | Devices by Type/ Windows Servers | isWindows()
- Remote Desktop Server | Devices by Type/ Windows Servers | isWindows()
- SQL Server (JDBC)| Devices by Type/ SQL Servers | hasCategory("MSSQL")  *For the latest MSSQL DataSources*

**vCenter Suite 1.0 Names | Expected dynamic group | Group definitions:**

- vCenter Capacity Utilization | Devices by Type/VMware vCenters | system.virtualization =~ "vCenter"
- vCenter Cluster Performance | Devices by Type/VMware vCenters | system.virtualization =~ "vCenter"
- vCenter Host Performance | Devices by Type/VMware vCenters | system.virtualization =~ "vCenter"
- vCenter Storage Performance | Devices by Type/VMware vCenters | system.virtualization =~ "vCenter"
- vCenter Virtual Machine Performance | Devices by Type/VMware vCenters | system.virtualization =~ "vCenter"
- vCenter VMware Overview | Devices by Type/VMware vCenters | system.virtualization =~ "vCenter"

**Custom Dashboard Names | Expected dynamic group names | Group definitions:**

- APC | Devices by Type/ APC | hasCategory("APC")
- Aruba Wireless | Devices by Type/ Aruba | hasCategory("Aruba")
- Brocade | Devices by Type/ Brocade | hasCategory("Brocade")
- Checkpoint | Devices by Type/ Checkpoint | system.sysoid == "1.3.6.1.4.1.2620.1.6.123.1.49"
- Cisco ASA | Devices by Type/ Cisco ASA | hasCategory("CiscoASA")
- Cisco WLC | Devices by Type/ Cisco WLC | system.displayname =~ "WLC"
- Dell iDRAC Hardware Status | Devices by Type/ Dell iDRAC | hasCategory("DellDRACDetail")
- EMC VNX | Devices by Type/ EMC | hasCategory("EMC") || hasCategory("EMC_VNX") || hasCategory("EMC_VNX2")
- F5 BIG-IP | Devices by Type/ F5 | hasCategory("F5")
- Fortinet Fortigate | Devices by Type/ Fortinet | hasCategory("Fortigate")
- LogicMonitor Portal Metrics | * | (Requires the LogicMonitor Portal Metrics custom datasource)
- Meraki | Devices by Type/ Meraki | hasCategory("MerakiCloudController")
- Meraki Expanded | Devices by Type/ Meraki | hasCategory("MerakiCloudController")
- Nimble Storage | Devices by Type/ Nimble | hasCategory("Nimble")
- Palo Alto | Devices by Type/ Palo Alto | hasCategory("PaloAlto")
- Pure Storage | Devices by Type/ Pure Storage | purestorage.apitoken.pass
- SonicWall | Devices by Type/ SonicWall | hasCategory("SonicWallFW")
- SQL Server (PerfMon) | Devices by Type/ SQL Servers | hasCategory("MSSQL")
- Ubiquiti Unifi | Devices by Type/ Ubiquiti Unifi | unifi.user && unifi.pass
- Under Utilized Devices - On-Prem | * | (Point at the device group you wish to target)
- Under Utilized Devices - Public Cloud | AWS or Azure account | (Requires a local collector to be installed and monitoring cloud VMs)
- VMware_ESXi | Devices by Type/ VMware Hosts | system.virtualization =~ "VMware ESXi Host" (ESXi-Only, v.3 modules)
- VMware_vCenter_v1 | Devices by Type/ VMware vCenters | system.virtualization =~ "VMware ESXi vCenter" (Uses v.2 modules)
- VMware_vCenter_v2 | Devices by Type/ VMware vCenters | system.virtualization =~ "VMware ESXi vCenter" (Uses v.3 modules)

**Dashboard Groups Info:**

*The Dashboard Groups directory contains merged groups/sets of dashboards packaged into a single JSON file:*
- LogicMonitor Dashboards 1.0 - this is an export of LM "version 1" default dashboards from a brand new LogicMonitor account.
- LogicMonitor Dashboards 2.0 - this is an export of LM "version 2" default dashboards from a brand new LogicMonitor account.
- Microsoft Suite 1.0 - a collection of Microsoft-technology-focused dashboards
- vCenter Suite 1.0 - a collection of vCenter-focused dashboards that target various elements of VMware infrastructure.

**Default Dashboards 1.0 Names | Expected dynamic group names | Group definitions:** (These are now older/archived)

- Alert Overview | * | (Works without credentials for all devices)
- Collector Summary | Devices by Type/ Collectors | hasCategory("Collectors")
- Linux Overview | Devices by Type/ Linux Servers | isLinux() 
- Network Overview | Devices by Type/ Network | isNetwork()
- VMware Overview | Devices by Type/ VMware Hosts | system.virtualization =~ "VMware ESX Host"
- Welcome | * | (Works without credentials for all devices)
- Windows Overview | Devices by Type/ Windows Servers | isWindows()
