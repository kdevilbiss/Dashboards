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