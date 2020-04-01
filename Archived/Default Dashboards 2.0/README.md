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
