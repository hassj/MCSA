# CHAPTER 1: INSTALLING WINDOW SERVER 2012R2

## Chapter 1.1: Commonly command

- checking network card on server
`netsh interface ipv4 show interfaces`

- set static IP for ethernet cart eth0
`netsh interface ipv4 set address name=eth0 source=static gateway=192.168.10.1 mask=255.255.255.0 adress=192.168.10.2`

- set ip address for dns SERVER
`netsh interface ipv4 add dnsserver name=eth0 address=192.168.10.254 index=1`

- checking hostname 
`hostname`

- change time zone
`control timedate.cpl `

- changing servername to sv-core1
``

## Chapter 1.2: NIC teaming

- Server local -> property -> click on nic teaming:disabled -> choosing NIC and named it then enabled it -> set IP for TEAMING NIC on Network and sharing center

