# CHAPTER 13: VPN and Maping Devcies

## Chapter 13.1: VPN PPTP

![vpn-pptp](https://github.com/hassj/MCSA/blob/main/image/13-vpn-pptp.JPG)

need create an user have netowrk access (remote access) permission. ``properties -> Dial-in -> tick on Allow access in Network Access Permission TAB``

enable ``remote access and routing feature`` role on server, then ``Routing and Remote Access" pane on Server enable dial-up or VPN

Setup connection for client on ``Network and sharing center`` to setup connection Point-to-Point tunelling protocol (PPTP)

## Chapter 13.2: VPN site-site

![vpn-site-site](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-site.JPG)

similar with client-site PPTP above

## Chapter 13.3: VPN Client-site (SSTP) or Client-Gateway

> this type of VPN connection require CA CERT and NAT Inbound

![vpn-site-gateway](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway.JPG)

- On DC create an OU used for VPN, allow remote access to network.

![vpn-site-gateway lab](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-2.JPG)

- Enable CA server role on DC

![vpn-site-gateway lab 2](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-3.JPG)

![vpn-site-gateway lab 3](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-4.JPG)

![vpn-site-gateway lab 4](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-5.JPG)

![vpn-site-gateway lab 5](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-6.JPG)

next page choose Enterprise CA -> Root CA -> Create Private key -> Enter common name for CA CERT

![vpn-site-gateway lab 6](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-7.JPG)

- Create Certificate  Template then release ` run -> mmc`

![vpn-site-gateway lab 7](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-8.JPG)

![vpn-site-gateway lab 8](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-9.JPG)

Then choose Manager -> IPSec -> Duplicate Template 

![vpn-site-gateway lab 9](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-10.JPG)

![vpn-site-gateway lab 10](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-11.JPG)

![vpn-site-gateway lab 11](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-12.JPG)

![vpn-site-gateway lab 12](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-13.JPG)

![vpn-site-gateway lab 13](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-14.JPG)

then choose ``SSTP `` on page Enable Certificate Templates

Request Cert for server from CA Server (DC )

![vpn-site-gateway lab 14](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-15.JPG)

then install it to Computer Account

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-16.JPG)

Then choosing Enroll from the Active Directory policy

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-17.JPG)

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-18.JPG)

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-19.JPG)

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-20.JPG)

- Enable RAS on server

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-21.JPG)

Configure IP release and choosing cert just requested recently

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-22.JPG)

Then restart RRAS and enable on interface WAN of Server VPN

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-23.JPG)

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-24.JPG)

and enable Http on Network Address Translate Properties pane -> restart RRAS

- on Client access to web adress of VPN server to download CERT ``http://vpn_server_IPAddress/certsrv`` ( maybe you need administrator account to download Certs)

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-25.JPG)

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-26.JPG)

Trust Root CA on Client, install it into computer account of local Computer

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-27.JPG)

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-28.JPG)

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-29.JPG)

Then add local host of VPN IPADDRESS on Client, this point you can make a connection to VPN server

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-30.JPG)

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-31.JPG)

In case cannot make connection successfully, it need create a registry record on client as bellow: Run -> Regedit -> HKEY-LOCAL-MACHINE -> SYSTEM -> CurrentControlSet -> Services -> SstpSvc -> Parameters , Keep creating a parameter 
parameters -> New -> DWORD32 bit of value ``NoCertRevocationCheck``

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-32.JPG)

Configure on Client connection VPN property 

![vpn-site-gateway lab 15](https://github.com/hassj/MCSA/blob/main/image/13-vpn-site-gateway-33.JPG)
