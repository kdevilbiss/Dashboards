# Dashboards

A collection of (tokenized) LogicMonitor dashboards that can be re-used across accounts. When importing, change the value of the ##defaultDeviceGroup## token (if needed) to select the relevant group of devices for which you wish to visualize data. These are officially unsupported - but LogicMonitor Support can always help with adjustments!

Most of these dashboards rely on both the latest versions of LogicMonitor datasources, and dynamic groups in the 'Devices by Type' device group. If these groups don't exist, they can be created using the out-of-box PropertySources from LogicMonitor together with the below documentation. [So make sure you have the latest PropertySources (and DataSources) from the repository!](https://www.logicmonitor.com/support/settings/logicmodules/keeping-your-datasources-up-to-date/)

To see a preview of what some of these dashboards look like, visit the [LogicMonitor Dashboard Gallery](https://www.logicmonitor.com/sales/dashboards/index.html).

**Default Dashboards 1.0 Names | Expected dynamic group names | Group definitions:**

- Alert Overview | * | (Works without credentials for all devices)
- Collector Summary | Devices by Type/ Collectors | hasCategory("Collectors")
- Linux Overview | Devices by Type/ Linux Servers | isLinux() 
- Network Overview | Devices by Type/ Network | isNetwork()
- VMware Overview | Devices by Type/ VMware Hosts | system.virtualization =~ "VMware ESX Host"
- Welcome | * | (Works without credentials for all devices)
- Windows Overview | Devices by Type/ Windows Servers | isWindows()

**Custom Dashboard Names | Expected dynamic group names | Group definitions:**

- Active Directory Overview | Devices by Type/ Domain Controllers | hasCategory("MicrosoftDomainController")
- APC Overview | Devices by Type/ APC | hasCategory("APC")
- Aruba Wireless Overview | Devices by Type/ Aruba | hasCategory("Aruba")
- Brocade Overview | Devices by Type/ Brocade | hasCategory("Brocade")
- Checkpoint Overview | Devices by Type/ Checkpoint | system.sysoid == "1.3.6.1.4.1.2620.1.6.123.1.49"
- Cisco ASA Overview | Devices by Type/ Cisco ASA | hasCategory("CiscoASA")
- Cisco WLC Overview | Devices by Type/ Cisco WLC | system.displayname =~ "WLC"
- Dell iDRAC Hardware Status | Devices by Type/ Dell iDRAC | hasCategory("DellDRACDetail")
- EMC VNX Overview | Devices by Type/ EMC | hasCategory("EMC") || hasCategory("EMC_VNX") || hasCategory("EMC_VNX2")
- Exchange Server Overview | Devices by Type/ Exchange Servers | hasCategory("MSExchange")
- F5 BIG-IP Overview | Devices by Type/ F5 | hasCategory("F5")
- Fortinet Fortigate Overview | Devices by Type/ Fortinet | hasCategory("Fortigate")
- Hyper-V Overview | Devices by Type/ Hyper-V | hasCategory("HyperV")
- Local Network Latency | * | (Works without credentials for all devices)
- LogicMonitor Portal Metrics | * | (Requires the LogicMonitor Portal Metrics custom datasource)
- Meraki Overview | Devices by Type/ Meraki | hasCategory("MerakiCloudController")
- Meraki Overview Expanded | Devices by Type/ Meraki | hasCategory("MerakiCloudController")
- Nimble Storage | Devices by Type/ Nimble | hasCategory("Nimble")
- Palo Alto Overview | Devices by Type/ Palo Alto | hasCategory("PaloAlto")
- Pure Storage Overview | Devices by Type/ Pure Storage | purestorage.apitoken.pass
- SonicWall Overview | Devices by Type/ SonicWall | hasCategory("SonicWallFW")
- SQL Server Overview | Devices by Type/ SQL Servers | hasCategory("MSSQL")
- SQL Server Overview (JDBC)| Devices by Type/ SQL Servers | hasCategory("MSSQL")  *For the latest MSSQL DataSources*
- Ubiquiti Unifi Overview | Devices by Type/ Ubiquiti Unifi | unifi.user && unifi.pass
- Under Utilized Devices - On-Prem | * | (Point at the device group you wish to target)
- Under Utilized Devices - Public Cloud | AWS or Azure account | (Requires a local collector to be installed and monitoring cloud VMs)
- Web Server Overview | Devices by Type/ Web Servers | hasCategory("MicrosoftIIS")
- Windows DHCP Server Overview | Devices by Type/ Windows Servers | isWindows()

**Dashboard Groups Info:**
*The Dashboard Groups folder has (at the moment) two files. They are groups/sets of dashboards packaged into a single JSON:*
- LogicMonitor Dashboards - this is an export of the default dashboards from a brand new LogicMonitor account.
- LogicMonitor After Dark - this is effectively version 2.0 of the above, an enhanced and all solid-darkBlue themed set of the default dashboards just mentioned.
