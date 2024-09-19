# CHAPTER 15: NETWORK ACCESS PROTECTION

## Implement NAP dhcp

Aiming to deployment all securing requirement for DHCP system, so all safty client will be received IP from DHCP server whereas unsafty client will not.

on server need to install some serices like: DHCP, network policy and access service, NAP health policy server, NAP enforcement on DHCP, system health validator

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-1.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-2.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-3.JPG)

Group policy management editor -> computer configuration -> policies -> windows setting -> security setting -> system service -> Network access protection agent 

Group policy management editor -> computer configuration -> policies -> windows setting -> security setting -> Network access protection -> NAP Client configuration

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-4.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-5.JPG)

then gpupdate /force

On First server install Network policies and access service 

server manager -> tools -> Network policy server 

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-6.JPG)

> Double check below step

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-7.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-8.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-9.JPG)

and click next for all till finish

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-10.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-11.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-12.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-13.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-14.JPG)

On dhcp server property on it

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-15.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-16.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-17.JPG)

![NAP dhcp](https://github.com/hassj/MCSA/blob/main/image/15-NAP-dhcp-18.JPG)

## Chapter 15.2: NAP for VPN

NAP for VPN will enable windows firewall for vpn client when connect vpn to server automatically.

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn.JPG)

On DC server create an vpn user, enable enterprise CA certs, On first server join domain then request certification from CA server, trust CA root, install Network policy service then configuring network policy and access services, configuring windows server, configuring system health validator

- On DC create an vpn user and allow access network, enable CA service 

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-1.JPG)

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-2.JPG)

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-3.JPG)

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-4.JPG)

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-5.JPG)

Configuring CA: Server Manager -> Tools -> certification Authority 

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-6.JPG)

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-7.JPG)

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-8.JPG)

On First Server add certification to ``Computer Account`` via snap in pane

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-9.JPG)

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-10.JPG)

Install NPS service on first server then  configuring as below:

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-11.JPG)

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-12.JPG)

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-13.JPG)

![NAP vpn](https://github.com/hassj/MCSA/blob/main/image/15-NAP-vpn-14.JPG)

