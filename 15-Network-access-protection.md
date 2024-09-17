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

