# CHAPTER 14: NETWORK POLICY SERVER

## Chapter 14.1: VPN server using RADIUS

![VPN-Radius](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius.JPG)

Create OU user used for VPN server and user on DC, allow remote network access.

![VPN-Radius](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-1.JPG)

Enable RADIUS client and NPS service on Server.

![VPN-Radius](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-2.JPG)

![VPN-Radius](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-3.JPG)

Enable VPN service on second SERVER, and configuring PPTP protocol for VPN service on it. notice make it work with RADIUS server.

Make a connection to vpn server from client windows

## Chapter 14.2: VPN using NPS

![VPN-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-NPS.JPG)

Creating User used to access VPN. Allow access NPS. then enable RAS and NPS services on it.

![VPN-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-NPS-2.JPG)

Open NETWORK policy server disable 2 policies as below:

![VPN-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-NPS-3.JPG)

Create new NPS policy as bellow: 

![VPN-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-NPS-4.JPG)

![VPN-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-NPS-5.JPG)

![VPN-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-NPS-6.JPG)

Chosing EAP authentication method 

![VPN-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-NPS-7.JPG)

Finally connect to vpn server for testing

![VPN-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-NPS-8.JPG)

![VPN-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-NPS-9.JPG)

## Chapter 14.3: Connect VPN using NPS and RADIUS

> when using RADIUS need enable DC SERVER

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS.JPG)

- On DC server create OU and group user as you want, allow remote access

- First Server join domain and enable NPS, RADIUS service role. NPS need to register to ACTIVE DIRECTORY using RADIUS, choosing Ms-Chapv2 authentication method

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-2.JPG)

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-3.JPG)

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-4.JPG)

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-5.JPG)

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-6.JPG)

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-7.JPG)

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-8.JPG)

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-9.JPG)

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-10.JPG)

Checking Created policies

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-11.JPG)

Installing RAS serice on second SERVER then enable VPN service, notice choose RADIUS server for authentication.

Finally, make a connection from client using Ms-Chapv2 authentication method.

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-12.JPG)

![VPN-RAIDUS-NPS](https://github.com/hassj/MCSA/blob/main/image/14-VPN-Radius-NPS-13.JPG)

