# CHAPTER 4: NETWORK MONITOR

this tool allows you to capture network traffic, analysis and filter that network traffic if needed. If using Active directory, should installing on DC server

[Network monitor tool](https://learn.microsoft.com/en-us/troubleshoot/windows-client/networking/collect-data-using-network-monitor)

you also use Wireshark tool 

# CHAPTER 5: DHCP

## Installing DHCP

Installing DHCP on AD, Configure DHCP relay agent, backup and restore DHCP server.

- Server Manager/Add roles and features -> choose DHCP role -> confirm and finish.

- Tool/dhcp -> new scope -> choose configuratino which you want

## DHCP relay agent

you need enable RRAS (Routing and Remote Access server) a function or application play role as router for control and route network traffic on Windows

![DHCP relay agent model](https://github.com/hassj/MCSA/blob/main/image/05-DHCP-relay-agent-model.JPG)

- In case your company have 1 DC controller server and one server windows (called win-server) used to install some features such as DHCP agent or WSUS....

![DHCP relay agent Ip adress pool](https://github.com/hassj/MCSA/blob/main/image/05-DHCP-AGENT-IPaDRESS-pool.JPG)

> Model: DC -(communicate)-> win-server (hav2 multiple NIC) - (CAN communicate with other server and clients)-> clients

- Step: Creating dhcp pool on DC -> enable RRAS (on win-server) -> enable feature on win-server then add new interface needed to manage the communication with each LAN network -> restart service on win-server

## Backing up and restoring the DHCP server

- Create a folder to store DATABASE backup of DHCP

- on DHCP panel click on dhcp server to backup and restore the database which you want.


## Failover DHCP

just need two DHCP servers, then enable failover feature on FIRST DHCP server to synchronyze to secondary DHCP server.

