# Dashboards

A collection of (tokenized) LogicMonitor dashboards that can be re-used across accounts. When importing, select the relevant group of devices for which you wish to visualize data. These are officially unsupported - but LogicMonitor support can always help with adjustments. 

Most of these dashboards rely on dynamic groups in the 'Devices by Type' device group - which can be created using the out-of-box PropertySources from LogicMonitor. (So make sure you have the latest PropertySources from the repository!)

To see a preview of what these dashboards look like, visit the [LogicMonitor Dashboard Portfolio](https://www.logicmonitor.com/sales/dashboards/index.html).

**Out-of-Box Dashboard Names | Expected dynamic group names | Group definitions:**

- Alert Overview | * | (Works without credentials for all devices)
- Collector Summary | Devices by Type/ Collectors | hasCategory("Collectors")
- Linux Overview | Devices by Type/ Linux Servers | isLinux() 
- Network Overview | Devices by Type/ Network | isNetwork()
- VMware Overview | Devices by Type/ VMware Hosts | system.virtualization =~ "VMware ESX Host"
- Welcome | * | (Works without credentials for all devices)
- Windows Overview | Devices by Type/ Windows Servers | isWindows()


**Custom Dashboard Names | Expected dynamic group names | Group definitions:**

- Active Directory Overview | Devices by Type/ Domain Controllers | hasCategory("MicrosoftDomainController")
- Cisco ASA Overview | Devices by Type/ Cisco ASA | hasCategory("CiscoASA")
- EMC VNX Overview | Devices by Type/ EMC | hasCategory("EMC") || hasCategory("EMC_VNX") || hasCategory("EMC_VNX2")
- Exchange Server Overview | Devices by Type/ Exchange Servers | hasCategory("MSExchange")
- Local Network Latency | * | (Works without credentials for all devices)
- Palo Alto Overview | Devices by Type/ Palo Alto | hasCategory("PaloAlto")
- SQL Server Overview | Devices by Type/ SQL Servers | hasCategory("MSSQL")
- Under Utilized Devices - On-Prem | * | (Point at the device group you wish to target)
- Under Utilized Devices - Public Cloud | AWS or Azure account | (Requires a local collector to be installed and monitoring cloud VMs)
- Web Server Overview | Devices by Type/ Web Servers | hasCategory("MicrosoftIIS")
